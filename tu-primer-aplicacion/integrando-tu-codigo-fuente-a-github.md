# 2.2 Integrando tu código fuente a GitHub

### 2.2.1 ¿Qué es GitHub?

Github es un sitio web en el cual puedes guardar y administrar el código de tus sistemas, puedes guardarlo de forma privada pra que solamente tu y los programadores de tu equipo de trabajo tengan acceso al código o de forma pública cuando deseas que tu código este disponible para cualquier persona. Algunos de los frameworks mas populares como Angular, Reac, .Net Core cuentan con el código público en GitHub. 

GitHub te permite además llevar un control de los bugs, o mejoras que deseas agregarle a tu sistema \(issues\), te presenta algunas estadísticas de cuantas veces se ha descargdo el proyecto, te permite agrear una wiki de tu proyecto que es donde se suele agregar la documentación de tu proyecto. 

### 2.2.2 Creando tu primer Aplicación

Para crear tu proyecto REST desde Visual Studio Comunity los pasos son los siguientes:

1. Ir al menú **Archivo** -&gt; **Nuevo** -&gt; **Proyecto**
2. Teclear el nombre del proyecto \(**CaducaRest**\) y la ubicación donde se creará el proyecto
3. Seleccionar la opción **Guardar**
4. Elegir **.NET Core 3.1** y seleccionar el proyecto de **API**. 
   1. Se recomienda usar los servicios REST con un certificado HTTPS si deseas manejarlo selecciona configure for HTPPS 

### 2.2.3 Instalar la extensión de GitHub

Para agregar tu proyecto a GitHub puedes descargar la extensión de GitHub.

1. Ir a **Herramientas** -&gt; **Extensiones y Actualizaciones**
2. En la pestaña de **En Línea** -&gt; **Buscar** -&gt; **GitHub** y dar clic en **Descargar**

![Figura 2.2.1 Obtener la extensi&#xF3;n de GitHub para Visual Studio Comunity](../.gitbook/assets/2018-08-30_1009.png)

Las extensiones se instalan al cerrar y volver a abrir el Visual Studio

1. Cerrar Visual Studio y volverlo a abrir. 
2. Dar clic en modificar
3. Dar clic en iniciar

### 2.2.4 Agregar tu proyecto a GitHub

1. Abrir tu proyecto 
2. Dar clic en el menú **Equipo**
3. **Administrar Conexiones**
4. Dar clic en **publish to GitHub**
5. Iniciar sesión con tu cuenta de GitHub
6. Seleccionar tu usuario, el nombre del repositorio y opcionalmente una descripción

![Figura 2.2.2 Iniciar sesi&#xF3;n con tu cuenta de GitHub](../.gitbook/assets/publica.png)

Listo tu proyecto se ha publicado en GitHub

### 2.2.5 Obtener el código desde Visual Studio for Mac

Para obtener el código fuente realizamos lo siguiente

1. En el menú **Control de Versiones** -&gt; **Extraer del repositorio**
2. En tipo Seleccionar **Git** 
3. En la URL seleccionamos la URL del proyecto de GitHub [https://github.com/apis3445/CaducaRest.git](https://github.com/apis3445/CaducaRest.git)
4. Seleccionar el directorio de destino donde deseas guardar el código
5. Dar clic en extraer del repositorio

![](../.gitbook/assets/image%20%28311%29.png)

