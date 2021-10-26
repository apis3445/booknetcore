# 10. Pruebas Unitarias

Como comente en la sección de código limpio todas tus funciones deben realizar una sola tarea, así es más fácil de probar.

Las pruebas unitarias deben probar únicamente alguna regla de negocio sin conexión con ningún proveedor externo como base de datos, servicios, la idea final es que todas las pruebas unitarias se corran muy rápido (en segundos) y se prueben las reglas de negocio de tu aplicación.

Las pruebas unitarias te ayudan a que cada vez que liberes una nueva versión del producto, verificar de  forma rápida que los cambios realizados no te agregarán nuevos bugs. Al ser automáticos no tienes que volver a probar manualmente cada vez que realizas un cambio.&#x20;

Puedes pensar que es mas tardado crear las pruebas automáticas, pero de todas formas debes probar el código. Es mejor probarlo y dejar documentado las reglas de negocio en tus pruebas, para cuando entra alguien más en el equipo sea mas fácil conocer las reglas. Conforme crece tu aplicación es mejor que se prueben automáticamente a probar manualmente.

Al final de la lección se verá como configurar Pipelines con BitBucket y Azure DevOps para que cada vez que un programador le da commit a sus cambios se corran en automático las pruebas automáticas.&#x20;

Puedes ver el siguiente video en inglés sobre pruebas unitarias, en el video podrás comprar un curso para ver el curso completo de pruebas unitarias.

{% embed url="https://www.youtube.com/watch?v=HYrXogLj7vg" %}
