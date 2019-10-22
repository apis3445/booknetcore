# 2.1 Integrando tu código fuente a Azure DevOps

Visual Studio Team Services ahora renombrado como Azure DevOps ya esta integrado a Visual Studio Comunity. Puedes crear tu cuenta aquí [https://visualstudio.microsoft.com/es/vso/](https://visualstudio.microsoft.com/es/vso/) y da clic en Comience a usarlo de forma gratuita.

Antes de empezar a programar es recomendable hacer una planeación de las tareas a realizar y quien las va a realizar. Las metodologías mas comunes actualmente son Agiles o Scrum. En este ejemplo utilizaré Scrum.

Antes de definir tus tareas o la forma de trabajar es importante pensar en quienes serán tus usuarios, que edad tienen, como es que utilizan el sistema, por ejemplo si siempre lo utilizan en un horario fijo en horario de oficina, si no sufren distracciones, o si para realizar una tarea deben comunicarse con otras personas, etc. 

Para nuestro ejemplo los usuarios podrían ser gerentes de farmacias de ciudades medianas y grandes, los cuales tienen una edad entre 30 y 35 años, los cuales deben revisar los productos próximos a caducar para ponerlos en oferta para que no caduquen.

En Scrum tu defines las tareas \(backlogs\) para ir entregando el sistema en tiempos cortos de dos semanas a un mes, con una funcionalidad básica e ir agregando mas funcionalidad en cada iteración \(sprint\), entre mas pronto entregues el software es más fácil realizar mejoras e ir revisando si se cumple con los requisitos y calidad que el cliente espera. Se recomienda ir clasificando tus tareas de forma jerárquica.

En las metodologías agiles se tiene también el concepto de User Stories los cuales son  descripciones breves y simples desde el punto de vista de la persona que desea una nueva función al sistema. Por  lo general es lo que el usuario o cliente del sistema desea, describiendo de forma general como trabaja y para que necesita el sistema.

{% hint style="info" %}
Una buena user story debe ser independiente, debe entregar algún valor al usuario, debe poder estimarse el tiempo que te llevará desarrollar la función, debe ser pequeña y se debe poder probar.
{% endhint %}

Se revisa con el cliente las prioridades a entregar en cada sprint. Se tienen elementos básicos

* **Epic:**  Es una colección de User Stories que pertenecen al mismo módulo o característica para alcanzar una meta. Por ejemplo serían todas las user stories para controlar la caducidad de los productos
* **Features:**  Representa una opción o componente del sistema que se va entregar por ejemplo: Agregar la opción de login, agregar un carrito de compras, etc.
* **Backlogs:** Es una lista de tareas \(user stories\) que necesitan realizarse en el proyecto para alcanzar la meta del producto. Por ejemplo un backlog podría ser el registro de nuevos usuarios
* **Task:** Son las tareas que se necesitan realizar en cada backlog. Para el ejemplo del registro de neuvos usuarios, las tareas podrían ser registro con Facebook, registro con Gmail, registro manual con correo, confirmación de email.

![Figura 2.2.1 Estructura de las actividades a realizar en Scrum](../../.gitbook/assets/scrum-2.png)



Puedes ver la documentación oficial aquí de momento solo esta en inglés

{% embed url="https://docs.microsoft.com/es-es/azure/devops/boards/backlogs/define-features-epics?view=azure-devops" %}



