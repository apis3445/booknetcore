# 12. Publicar tus Servicios REST en Azure

Puedes publicar tu sitio web en azure de forma gratuita. Si nunca has utilizado Azure se te da un año gratuito para que conozcas Azure y pruebes los diferentes servicios con los que cuenta. Se te pedirá tarjeta de crédito. Crea y registra tu cuenta en Azure en el siguiente link

{% embed url="https://azure.microsoft.com/es-es/" %}

Para publicar nuestros servicios rest vamos a utilizar el servicio App Service.

![](../.gitbook/assets/image%20%28102%29.png)

Da clic en el botón Crear App Service

![](../.gitbook/assets/image%20%28372%29.png)

LLena los datos que se te solicitan

![](../.gitbook/assets/image%20%28138%29.png)

**Suscripción**: Selecciona tu suscripción en mi caso se llama Pago por uso ya que ya utilice la cuenta gratuita.

**Grupo de recursos:** Azure te permite agrupar tus servicios por grupos para por ejemplo si tienes muchos clientes diferentes los agrupas por cliente.

**Nombre**: agrega el nombre que dseeas para tus servicios en mi caso es caducarest

**Publicar**: Selecciona Código, otra opción de publicar tu código es mediante docker, el cual como su nombre lo dice es un contenedor que previamente configuras con todo lo necesario para publicar tus servicios, el tema de docker se verá en otra sección

**Pila del entorno en tiempo de ejecución**: Selecciona la versión de .net Core, en mi caso estoy utilizando la versión .Net Core 3.1.

**Sistema Operativo**: Selecciona Linux ya que suele ser mas económico

**Región**: Selecciona una región cercana a la ciudad donde vives

Selecciona un nuevo plan, en mi caso le llame Linux. Cambia la sugerencia de un servicio Premium, dando clic en Cambiar el tamño, se te abre al lado derecho para que elijas la opción en mi caso elegiré un plan gratuito, el cual solo tiene 1 GB de meoria. 

Da clic en **Aplicar** y luego en **Revisar y crear**

![](../.gitbook/assets/image%20%2836%29.png)

Por último da clic en crear y espera un momento en lo que Azure prepara todo para que puedas publicar tus servicios.

