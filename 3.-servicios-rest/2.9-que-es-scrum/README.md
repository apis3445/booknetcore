# 2.9 ¿Qué es Scrum?

Antes de empezar a programar es recomendable hacer una planeación de las tareas a realizar y quien las va a realizar. Las metodologías mas comunes actualmente paraa desarrollar son Agiles o Scrum. Solo daré una explicación general ya que es un tema muy amplio.

Una vez que eliges la metodología es importante analizar y que quede claro para todos los miembros del equipo quienes son tus usuarios \(Personas\) por ejemplo debes definir lo siguiente:

* A quien va dirigido el sistema: Debes saaber quien va a utilizar el sistema si son ejecutivos, gerentes, o personal administrativo. Ya que por lo general un gerente desea ver mas información mas resumida, y alguien administrativo desea poder registraar la información de forma más rápida.
* Su Edad: Por ejemplo si son personas mayores debes por ejemplo pensar en utilizaf un tamaño de letra mas grande y talves incluir muchas ayudas visuales.  Si es alguien muy joven puedes  pensar en diseños mas sencillos que puedan verse en celular de forma muy rápida.
* Como es su día a día utilizando el sistema: Por ejemplo si siempre lo utilizan en un horario fijo en horario de oficina, si no sufren distracciones, o si para realizar una tarea deben comunicarse con otras personas, etc. 

Ejemplo de Personas:

Los usuarios podrían ser gerentes de farmacias de ciudades medianas y grandes, los cuales tienen una edad entre 30 y 35 años, los cuales deben revisar los productos próximos a caducar para ponerlos en oferta para que no caduquen.

La idea del Scrum es ir entregando las funciones del sistema en tiempos cortos de dos semanas a 6 semanas, con una funcionalidad básica e ir agregando mas funcionalidad en cada iteración \(sprint\), entre mas pronto entregues el software es más fácil realizar mejoras e ir revisando si se cumple con los requisitos y calidad que el cliente espera. 

Una vez que queda claro quienes serán los usuarios y la duración del sprint y los miembros del equipo, se definen las tareas, las cuales se pueden clasificar de la siguiente manera:

* **User Stories:** Es una lista de tareas que necesitan cumplirse en el sprint, debe ser de utilidad para el usuario.  Ejemplos: 
  * Registrar los usuarios con correo electrónico
  * Registrar los usuarios con Facebook.
* **Task:** Son las tareas que se necesitan realizar para el User Story. Las tareas deben ser completadas en máximo un día de trabajo. Las tareas se pueden ir detallando antes del inicio de cada sprint. No se trata de detallar todo el sistema en un inicio si no ir agregando los detalles poco a poco. Ejemplos:
  * User Story: Registrar los usuarios con correo electrónico Tasks \(Tareas\):
    * Crear el script de la base de datos para registrar la tabla de usuarios.
    * Crear el servicio para registrar los usuarios.
    * Crear el componente en Angular
    * Crear las pruebas unitarias para el servicio
    * Crear las pruebas con protactor.
* **Features:**  Como el sprint se trata de dividir una tarea en tareas mas sencillas, para ir entregando un producto minimo viable \(MVP\) y luego irle agregando mas funcionalidad, el feature es una colección de User Stories.El feature terminado puede terminarse en varios sprint.  Ejemplos:
  * Feature: Opción para registrar usuarios User Stories
    * Registrar los usuarios con correo electrónico
    * Registrar los usuarios con Facebook
    * Registrar los usuarios con Google
    * Registrar los usuaarios con Linkedin
* **Epic:**  Es una colección de User Stories que pertenecen al mismo módulo o característica para alcanzar una meta. Por ejemplo serían todas las user stories para controlar la caducidad de los productos

![](../../.gitbook/assets/image%20%28438%29.png)

Una vez definido se registran las tareas en un backlog que contiene la lista de las user story con prioridad, asi el equipo de desarrollo puede ir tomando las tareas mas importantes primero y cuando termina una puede tomar la siguiente disponible.

### Recomendaciones para crear User Stories  

Se recomienda que las User Stories sean:

* Ser independiente, no debe interferir con otras user stories
* Entregar algún valor al usuario y debe ser algo que el usuario pueda probar y utilizar.
* Debe terminarse durante un sprint.
* Deben definirse los criterios de aceptación, el cual es un checklist con la funcionalidad que el usuario espera.

Se revisa con el cliente las prioridades a entregar en cada sprint. Se tienen elementos básicos para clasificar el trabajo.

Puedes ver la documentación oficial aquí de momento solo esta en inglés

{% embed url="https://docs.microsoft.com/es-es/azure/devops/boards/backlogs/define-features-epics?view=azure-devops" %}

#### Ejemplo de un User Story

Para la aplicación de ejemplo un User Story sería:

Nombre: Servicio para registrar las categorías de los productos

Descrición: Un usuario de tipo Administrador registra las categorías de todos los productos,  de esta manera mas adelante podrá asignar a cada vendedor las categorías de productos que debe vender y cuidar la fecha de caducidad.

Criterio de Aceptación: Debe validar que solo los usuarios de tipo administrador tengan acceso a esta opción en el menú.

Se deben crear, modificar y borrar categorías. 

Si un usuario no es administrador y quiere acceder a la página directamente debe mostrarle un error

Prioridad: 1

Puedes ver los siguientes links en inglés para aprender mas sobre scrum y las buenas prácticas

{% embed url="https://docs.microsoft.com/en-us/azure/devops/learn/agile/what-is-scrum" %}

{% embed url="https://docs.microsoft.com/es-mx/azure/devops/boards/sprints/best-practices-scrum?view=azure-devops" %}

