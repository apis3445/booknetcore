# 13. Integración continua con Postman

Puedes utilizar postman para probar tus tests y configurar el pipeline para que se ejecuten los scripts de postman después de actualizar la nueva versión de tu sistema.

Postman también cuenta con opciones:

* **Monitorear**: Configuras cada cuando deseas que se corran tus servicios. Para comprobar que tus servicios siempre estén disponibles.
* **Documentar**: Adicional a swagger puedes documentar los servicios y las pruebas que vas creando y compartirlo con los demás miembros del equipo.
* **Mock**: Puedes agregar json de ejemplo para simular llamadas a un servicio. Esto puede ser util para empezar a programar las pruebas en donde se tiene un equipo de developers y un equipo de testers.
* **Diseñar**: Mediante OpenApi un formato para definir tus APIS con yaml o con Json puedes diseñar el servicio y a partir de ese archivo puedes crear tus colecciones para probar tus servicios, la documentación y simular los servicios (mock)

{% hint style="info" %}
Postman utiliza javascript para las pruebas.
{% endhint %}

