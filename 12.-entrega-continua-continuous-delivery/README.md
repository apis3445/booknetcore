# 15. Despliegue Continuo con Azure DevOps y Azure

Una parte interesante de la entrega continua es que puedes configurar tus diferentes ramas, para que se publiquen por ejemplo a un servidor de pruebas cuando los programadores realizan un cambio en el código, y adicionalmente puedes correr las pruebas de postman o de selenium de forma automática.

Para la rama con la versión final de tu proyecto, puedes crear una regla para que la publicación sea de forma manual,  después de que haya sido aprobada por uno o mas miembros del equipo.

Mediante las migraciones puedes crear y ejecutar el script para actualizar la base de datos después de cada deploy.

También te genera un resumen de las tareas que se han cambiado en cada release.

Puedes generar con el mismo código una versión para un servidor linux y para windows.

### Ventajas

Algunas de las principales ventajas son las siguientes:

* El tiempo para desplegar tus aplicaciones es más rápido y lo puedes programar automáticamente a determinada hora.
* Las pruebas automáticas se ejecutan automáticamente y se puede hacer un rollback al deploy si no pasan las pruebas.
* Al ser un proceso automático se tienen menos errores por olvido o cambio en la ejecución de los pasos.&#x20;
* Si utilizas también la parte de scrum en azure devops tienes el  detalle de los user stories que se incluyen en cada versión de forma automática.

{% hint style="info" %}
Puedes realizar lo mismo con BitBucket, GitLab y GitHub Actions.
{% endhint %}
