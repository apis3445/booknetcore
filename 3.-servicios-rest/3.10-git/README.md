# 3.9 Git

### ¿Qué es Git?

Git es un sistema de control de versiones, es decir es un sistema que te permite controlar los cambios que haces a tu código, te facilita saber que cambios se hicieron al código, quien realizo el cambio, y puedes tener una copia del código por cada versión que tienes de tu sistema, asi puedes agregar correcciones a tu sistema, mientras continuas trabajando en las nuevas funciones. Para poder realizar esto se tiene el concepto de branches \(ramas\).  Git trabaja de forma local, por lo cual puedes tener versiones de tu código de forma local, las cuales después puedes sincronizar con algún repositorio remoto como Github, BitBucket.

### ¿Qué son las ramas en Git?

Por lo general se tiene el código de esta manera para que todos los programadores cuenten con el código del proyecto y poder controlar los cambios que cada persona realiza, y poder regresar a una versión anterior o que sea más fácil de revisar que es lo que cambio el código entre una versión y otra del sistema. 

Por lo general una forma de trabajar en equipos grandes de desarrollo es mediante ramas \(Branches\), que te permite crear copias de tu código para tener por ejemplo el código tal cual como esta en producción el sistema \(master\), y otra copia \(rama\) que se suele llamar develop\(desarrollo\) donde se tienen los cambios que los programadores estan realizando, también se suele tener una rama con cada versión liberada. Asi si vendes tu producto y cobras por versiones del mismo y ocurre un error en alguna versión puedes solo corregir ese error sin pasar todos los cambios de tus nuevas versiones. 

También para la rama de desarrollo una forma de trabajar es que cada programador descarga ua copia de la rama de desarrollo hace sus cambios y luego crea un pull request que es una petición para informar a los demás programadores o a tu jefe, que ya terminaste tus cambios y por lo general otro programador o analista revisa tus cambios y los aprueba \(Approve\) o te sugiere mejoras a tu código antes de agregar tus cambios a la rama de desarrollo.

Se tienen varios comandos para comparar el código entre las 2 ramas y actualizar el código de una rama a otra.

Si 2 personas realizan un cambio sobre el mismo archivo git te detecta el cambio y te pide que hagas un Merge que básicamente debes elegir si los 2 programadores cambiaron el mismo archivo cual código es el que se debería quedar.

 

![Diagrama de C&#xF3;digo en git con diferentes ramas \(branches\)](../../.gitbook/assets/image%20%28323%29.png)

### Comandos git 

Git cuenta con varios comandos para crear y ver las ramas y subir tus cambios.Algunos de los mas utilizados son los siguientes:

| Comando | Descripción |
| :--- | :--- |
| git clone &lt;url&gt; | Permite conocer un repositorio donde url es la dirección del repositorio que deseas clonar. |
| git branch | Permite ver la lista de ramas. La rama con \* es la rama actual. |
| git branch &lt;nombre&gt; | Permite crear una nueva rama a partir de la rama actual. |
| git checkout &lt;nombre&gt; | Permite cambiarte a la rama, solo debes indicar el nombre de la rama a la cual quieres cambiarte |
| git add . | Agrega todos los archivos que han sido cambiados, para luego confirmar los cambios con git commit. |
| git add &lt;archivo&gt; | Agrega el archivo que le pases como parámetros |
| git commit -m "mensaje" | Agrega todos los archivos con un mensaje, por lo general el mensaje es una descripción del cambio que se realiza |
| git push origin &lt;nombre&gt; | Agrega tus cambios a la rama con el nombre pasado como parámetro en el servidor remoto. |
| git fetch origin | Descarga la lista de cambios que tiene el servidor remoto que aún no estan en tu repositorio local |
| git pull origin &lt;nombre&gt; | Descarga los cambios del repositorio remoto a tu repositorio local |

