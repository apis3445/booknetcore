# 4.7 Mejorando tu código

A continuación, vamos a mejorar el código para prepararlo para pruebas unitarias y que cumpla con los principios de un código limpio.

Lo primero que vamos a hacer es separar el acceso a la base de datos de los servicios de esta forma al llegar a la parte de pruebas unitarias podemos probar de forma separara la base de datos y los servicios. Así si hay un error en un servicio podemos detectar de forma más fácil si el error está en la lógica del servicio o en la base de datos.

Después vamos a crear un archivo de recursos para manejar todos los mensajes de error de forma general, y esto también nos permite en un futuro tener los mensajes de error en diferentes idiomas.

