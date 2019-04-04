# 11.1 Creando una máquina virtual linux en Azure

Por lo general Azure tiene promociones para que pruebes sus productos gratuitos. 

* Por ejemplo la suscripción [DevEssentials](https://visualstudio.microsoft.com/es/dev-essentials/) tiene muchos beneficios aparte de Azure algunos días gratis de [Pluralsight](https://www.pluralsight.com), [Linkedin learning](https://www.linkedin.com/learning/me)
* Programas para emprendedores como [bizspark](https://startups.microsoft.com/es-es/) 
* Simplemente entradno a la página de [Azure](https://azure.microsoft.com/es-es/)
* Por medio de concursos en su página o redes oficiales.

Una vez que hayas elegido algún programa de beneficios gratuitos entra al portal de azure [https://portal.azure.com](https://portal.azure.com/signin/index/)

### Pasos para crear tu máquina virtual de Linux en Azure

1. Ingresa a tu portal de azure [http://portal.azure.com/](http://portal.azure.com/)
2. Da clic en Máquinas virtuales

![](../.gitbook/assets/image%20%2874%29.png)

3. Da clic en Agregar

![](../.gitbook/assets/image%20%2825%29.png)

4. Selecciona los datos generales:

* _Suscripción_: En mi caso tengo la de BizSpark
* _Grupo de recursos_: Es una clasificación para agrupar tus recursos, en mi caso le puse mi nombre
* _Nombre de máquina virtual:_ Un nombre para tu máquina virtual, en mi caso le llame AbiLinux
* _Región_: Busca una región cercana a tu ciudad, en mi caso seleccione Centro de EE-UU.
* _Imagen_: Selecciona el sistema operativo en mi caso elegi Ubuntu Server 18.04 LTS

![](../.gitbook/assets/image%20%2877%29.png)

5. Selecciona los siguientes datos:

* _Tamaño_: Elige el número de procesadores y de memoria, linux es realmente mas ligero a Windows por lo cual con 2 cpus y 7 GB de memoria esta bien, aunque puedes elegir alguna versión mas sencilla 
* Tipo de autenticación: Es más seguro utilizar una Clave pública SSH pero requere mas configuración, por motivos de hacer un tutorial más fácil elegire Contraseña
* Nombre de usuario: Elige un nombre de usuari, por motivos de sencilles elegi abi mas se recomienda un nombre mas elaborado
* Contraseña: Debe estar entre 12 y 72 caracteres de longitud, incluir mayúsculas, minúsculas, caracteres especiales
* _Puertos de entrada públicos_: Aquí selecciona todos para habilitar el acceso por SSH el cual es necesario ya que por defecto no se habilita el acceso remoto en las máquinas virtiales de linux, HTTP para tener tus servicios disponibles, HTTPS ya que se recomienda utilizar certificados SSL para tus servicios REST, y RDP para habilitar el escritorio remoto.

![](../.gitbook/assets/image%20%2848%29.png)

6. Da clic en el botón siguiente Discos

7. Puedes agregar un disco de datos para tener tus archivos de documentos y/o código separados del sistema operativo, asi si luego cambias de máquina virtual puedes solamente agregar el disco duro con tu información. Da clic en siguiente Redes

![](../.gitbook/assets/image%20%2852%29.png)

8. A continuación configuraremos la sección Redes, dejamos las opciones por default y nos aseguramos que aún este habilitados los puertos de HTTP, RDP, HTTPS, SSH

![](../.gitbook/assets/image%20%281%29.png)

9. En administración puedes activar la opción de apagado automático, esto es útil ya que solo pagas por el uso, si la apagas por ejemplo de 12:00 am a 6:00 am esas 6 horas no se te cobran.

10. Da clic en revisar y crear, te muestra un resumen con las opciones seleccionadas y te manda una notificación una vez que la máquina virtual este lista

![](../.gitbook/assets/image%20%2875%29.png)

