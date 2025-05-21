# 9.2 Seguridad basada en roles y usuarios

Una forma fácil de manejar la seguridad es mediante roles, para nuestro ejemplo vamos a tener los siguientes roles de usuarios:

* **Administradores**: Pueden consultar y modificar cualquier información en el sistema.
* **Vendedores**: Se encargan de registrar la caducidad de los productos de cada cliente. Por  ejemplo, el vendedor de la farmacia 1, no puede registrar productos en la farmacia 2, ni puede crear nuevos clientes.
* **Clientes**: Solamente pueden comprar productos. Por simplicidad del proyecto no creare los servicios de las ventas. Como ejercicio adicional puedes crear los servicios y tablas.

De esta manera cuando un usuario inicia sesión aparte de regresar el id del usuario, regresas la lista de roles que tiene el usuario, así en cada petición el servidor puede validar el rol que tiene el usuario en el token y si tiene el rol adecuado muestra la información.

Hay diferentes formas para manejar la seguridad y conectarte a algún servicio. Por ejemplo para facebook, twitter, google debes registrarte como desarrollador en sus páginas. Por lo general te piden un aviso de privacidad disponible en la página de tu sistema, explicas para que quieres conectarse a sus servicios. Después de aprobarte te dan un Id de tu aplicación y una clave secreta que debes enviar en cada petición.

Para tu aplicación debes seguir la documentación de cada proveedor y básicamente le das la opción al usuario de iniciar sesión con tu cuenta de google, facebook, etc se les muestra la opción para que inicien sesión con su cuenta y los permisos a los que permites que tenga acceso la aplicación. Como programador debes obtener el token que te regresa el login del usuario y también debes enviarlo en cada petición. Una página que explica bien es la de google.&#x20;

[https://developers.google.com/workspace/gmail/api/guides](https://developers.google.com/workspace/gmail/api/guides)

{% hint style="info" %}
Si deseas que luego incluya un tema para iniciar sesión con google, facebook, twitter o cualquier otro proveedor puedes solicitarlo en el github del código fuente
{% endhint %}

Esta forma es recomendada si deseas que varios proveedores externos accedan a tus servicios. Si solamente deseas que tu aplicación web/app propia accedan a tus servicios puedes utilizar solamente los Json Web Tokens  explicada en la sección de [seguridad](../)

Los siguientes capítulos muestran como crear tu seguridad de una forma muy personalizada .Net cuenta con su propio modelo de seguridad, se llama **Identity**, la documentación oficial esta aquí

[https://learn.microsoft.com/es-mx/aspnet/core/security/authentication/identity?view=aspnetcore-9.0\&tabs=visual-studio](https://learn.microsoft.com/es-mx/aspnet/core/security/authentication/identity?view=aspnetcore-9.0\&tabs=visual-studio)

Puedes ver un tutorial en ingles aquí

{% embed url="https://nbarbettini.gitbooks.io/little-asp-net-core-book/content/chapters/security-and-identity/" %}





