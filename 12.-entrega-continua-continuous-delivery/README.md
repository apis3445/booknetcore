# 15. Despliegue Continuo con Azure DevOps y Azure

Una parte interesante de la entrega continua es que puedes configurar tus diferentes ramas, para que se publiquen por ejemplo a un servidor de pruebas cuando los programadores realizan un cambio en el código, y adicionalmente puedes correr las pruebas de postman o de selenium de forma automáticas.

La rama con la versión final de tu proyecto, puedes crear una regla para que la publicación sea de forma manual, solamente después de que haya sido aprobada por uno o mas miembros del equipo.

También mediante las migraciones puedes crear y ejecutar el script para actualizar la base de datos después de cada deploy.

También te genera un resument de las tareas que se han cambiado en cada release.

También por ejemplo puedes generar con el mismo código una versión para un servidor linux, otra para windows.

### Ventajas

Algunas de las principales ventajas son las siguientes:

* El tiempo para desplegar tus aplicaciones es más rápido y lo puedes programar automáticamente a determinada hora.
* Se tienen menos errorres, lo que da mas seguridad de no agregar nuevos bugs debido a las pruebas automáticas
* Por lo general se liberan versiones continuamente y recibes el feedback más rápido.
* Al utilizar Azure Devops tienes el control de que cambios se incluyen en cada versión de forma automática de acuerdo a los task.

{% hint style="info" %}
Puedes realizar lo mismo con BitBucket, GitLab y GitHub Actions.
{% endhint %}

