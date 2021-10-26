# 14.2 ¿Qué es Selenium?

Selenium es una suite de herramientas que te permite automatizar tus pruebas en diferentes navegadores.También cuenta con librerías para ejecutar estas pruebas con los lenguajes mas utilizados como C#, Java, Python.

Cuenta con extensiones para Firefox y Chrome en el cual puedes grabar los pasos que realizas en alguna página web y las puedes ejecutar cuando lo desees.

Ventajas

1. Cuenta con locator relativos, por lo cual puedes elegir elementos como el elemento arriba del botón login.
2. Soporta varios lenguages Java, C#, Python, Ruby.
3. Soporta varios navegadores Chrome, Safari, Firefox, Internet Explorer, Edge, Opera

Deventajas

1. No cuenta con una herramienta para el reporte de las pruebas
2. Es difícil probar aplicaciones complejas por ejemplo grids o componentes como AutoComplete, TreeViews.
3. Es difícil detectar si la información se esta cargando, por lo que debes agregar código para esperar a que el elemento este visible, habilitado, etc.
4. No puedes crear test de servicios REST o SOAP, como  cypress para modificar la respuesta de los servicios o ejecutar un test en cuanto un servicio REST o SOAP regresa la informacion.

