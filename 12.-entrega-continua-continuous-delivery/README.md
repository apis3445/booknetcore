# 15. Despliegue Continuo con Azure DevOps y Azure

Una parte interesante de la entrega continua es que puedes configurar tus diferentes ramas, para que se publiquen por ejemplo a un servidor de pruebas cuando los programadores realizan un cambio en el código, y adicionalmente puedes correr las pruebas de postman o de selenium de forma automática.

Para la rama con la versión final de tu proyecto, puedes crear una regla para que la publicación sea de forma manual,  después de que haya sido aprobada por uno o mas miembros del equipo.

Mediante las migraciones puedes crear y ejecutar el script para actualizar la base de datos después de cada deploy.

También te genera un resumen de las tareas que se han cambiado en cada release.

Puedes generar con el mismo código una versión para un servidor linux y para windows.

### Ventajas

Algunas de las principales ventajas son las siguientes:

* El tiempo para desplegar tus aplicaciones es más rápido y lo puedes programar automáticamente a determinada hora.
* Se tienen menos errorres antes del release debido a las pruebas automáticas.
* Por lo general se liberan versiones continuamente y recibes el feedback más rápido.
* Al utilizar Azure Devops tienes el control de que cambios se incluyen en cada versión de forma automática de acuerdo a los task.

{% hint style="info" %}
Puedes realizar lo mismo con BitBucket, GitLab y GitHub Actions.
{% endhint %}
