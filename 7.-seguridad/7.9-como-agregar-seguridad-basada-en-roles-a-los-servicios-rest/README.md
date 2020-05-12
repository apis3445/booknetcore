# 7.5 ¿Cómo agregar seguridad basada en roles a los Servicios REST?

Agregar la seguridad basada en roles a nuestros servicios es muy fácil con .NET, lo único que debemos agregar es entre \[\] la palabra Authorize y entre \(\) agregamos la palabra Roles = y separados por comas agregamos los roles que pueden acceder al servicio.

En nuestro archivo **CategoriasController** validamos que solamente los usuarios de tipo administrador y de ventas puedan ver las categorías de los productos.

{% code title="CategoriasController.cs" %}
```csharp
[HttpGet]
[Authorize(Roles = "Administrador, Ventas")]
public List<Categoria> GetCategoria()
{
      return categoriaDAO.ObtenerTodo();
}
```
{% endcode %}

Si probamos nuestro servicio de **GetCategoria** con un usuario de tipo Cliente el servicio nos regresará un status **403 Forbidden** ya que aunque es un usuario correcto no tiene permiso para consultar esa información

Si deseas agregar la autorización a todos los servicios del controller, agregas los roles directamente al Controller. 

{% code title="ProductosController" %}
```csharp
[Authorize(Roles = "Administrador")]
public class ProductosController : ControllerBase
{
}
```
{% endcode %}

Para nuestros servicios con OData es lo mismo, agregamos la autorización ya sea al controller o al método

{% code title="ClientesController.cs" %}
```csharp
[Authorize(Roles = "Administrador")]
public class ClientesController : ODataController
{
}
```
{% endcode %}

Si deseas que un servicio solo sea accesible si el usuario tiene 2 roles los agregas uno abajo de otro. Por ejemplo los siguientes servicios solo son accesibles si el usuario tiene el rol de Admin y de ControlPanel

```csharp
[Authorize(Roles = "Admin")]
[Authorize(Roles = "ControlPanel")]
public class ControlPanelController : Controller
{
}
```

Puedes ver la documentación de microsoft aquí.

{% embed url="https://docs.microsoft.com/es-es/aspnet/core/security/authorization/roles?view=aspnetcore-2.2" %}

