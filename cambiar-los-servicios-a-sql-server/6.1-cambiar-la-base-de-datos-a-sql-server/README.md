# 6.1 Cambiar la base de datos a SQL Server

Cambiar de base de datos es relativamente fácil, primero cambiaremos la base de datos a un SQL Server local y luego un SQL Server en Azure

1\) Agrega el siguiente paquete Nuget  

```text
Install-Package Microsoft.EntityFrameworkCore.SqlServer
```

2\) Creamos la base de datos en sql server y nuestros usuarios administrador y de lectura

{% code-tabs %}
{% code-tabs-item title="CaducaSQLBD.sql" %}
```sql
//Creamos la base de datos
CREATE DATABASE caduca
GO
//Creamos un login para el usuario administrador
CREATE LOGIN AdminCaduca WITH PASSWORD = 'StKRV6MR6A'
GO
//Creamos un login para el usuario de lectura
CREATE LOGIN SistemaCaduca WITH PASSWORD = 'xADcUaP5cs'
GO
//Cambiamos a la base de datos
USE caduca
GO
//Creamos los usuarios administrador y de sistema
CREATE USER AdminCaduca FOR LOGIN AdminCaduca;
CREATE USER SistemaCaduca FOR LOGIN SistemaCaduca;
//Agreamos el permiso al usuario administrador de db_owner el cual 
//tiene acceso total a la base de datos
ALTER ROLE db_owner ADD MEMBER AdminCaduca;
//Agregamos los roles de escritura y lecutra para el 
// usuario de sistema
ALTER ROLE db_datareader ADD MEMBER SistemaCaduca;
ALTER ROLE db_datawriter ADD MEMBER SistemaCaduca;
```
{% endcode-tabs-item %}
{% endcode-tabs %}

3\) Agregamos una nueva cadena de conexión en nuestro archivo appsettings.json con el nombre **SQLServerConnection** 

{% code-tabs %}
{% code-tabs-item title="appsettings.json" %}
```javascript
{
  "ConnectionStrings": {
    "DefaultConnection": "server=localhost;port=3306;database=caduca;user=AdminCaduca;Password=StKRV6MR6A;sslMode=none",
    "SQLServerConnection": "Server=localhost;Database=caduca;User Id=AdminCaduca;Password=StKRV6MR6A;"
  },
  //...
}

```
{% endcode-tabs-item %}
{% endcode-tabs %}

4\) Cambiamos nuestro archivo **Startup.cs** para que utilice Sql Server, dejamos comentada nuestra conexión MySQL por si deseamos regresar a MySQL y nuestra nueva cadena de conexión

{% code-tabs %}
{% code-tabs-item title="Startup.cs" %}
```csharp
public void ConfigureServices(IServiceCollection services)
{
    //Código
    
    //Conexión MySQL
    //services.AddDbContext<CaducaContext>(options => 
           //options.UseMySql(Configuration.GetConnectionString
           //("DefaultConnection")));
   
    //Conexión SQL Server
    services.AddDbContext<CaducaContext>(options =>
         options.UseSqlServer(Configuration.GetConnectionString
              ("SQLServerConnection")));
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

5\) Modificamos nuestra migración para que cree correctamente el campo autoincrement, ya que se agrego una notación especial para MySQL  \(**.Annotation\("MySql:ValueGenerationStrategy", MySqlValueGenerationStrategy.IdentityColumn\)**\) agregamos el código para generar el identity en sql Server **.Annotation\("SqlServer:ValueGenerationStrategy", SqlServerValueGenerationStrategy.IdentityColumn\)**

{% code-tabs %}
{% code-tabs-item title="Migracion\_TablaProducto.cs" %}
```csharp
migrationBuilder.CreateTable(
    name: "Producto",
    columns: table => new
    {
        Id = table.Column<int>(nullable: false)
        .Annotation("SqlServer:ValueGenerationStrategy", 
         SqlServerValueGenerationStrategy.IdentityColumn),
        // .Annotation("MySql:ValueGenerationStrategy"
        //, MySqlValueGenerationStrategy.IdentityColumn),
   }
```
{% endcode-tabs-item %}
{% endcode-tabs %}

También modificamos la migración de la TablaCategoría de la misma forma

6\) Ejecutamos el comando **Update-Database** en la **Consola del Administrador de Paquetes**

Listo hemos cambiado la base de datos a SQL Server.

