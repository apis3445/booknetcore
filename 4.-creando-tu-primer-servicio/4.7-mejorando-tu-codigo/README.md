# 4.7 Mejorando tu código

Si tu aplicación es muy pequeña y no necesitas realizar pruebas unitarias puedes utilizar el código generado por visual studio.&#x20;

A continuación, vamos a mejorar el código para prepararlo para pruebas unitarias y que cumpla con los principios de un código limpio.

Lo primero que vamos a hacer es separar el acceso a la base de datos de los servicios de esta forma al llegar a la sección de pruebas podemos probar de forma separada la base de datos y los servicios. Si hay un error en un servicio podemos detectar de forma más fácil si el error está en la lógica del servicio o en la base de datos.

Después vamos a crear un archivo de recursos para manejar todos los mensajes de error de forma general. Esto también nos permite en un futuro tener los mensajes de error en diferentes idiomas.
