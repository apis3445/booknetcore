# 4. Creando tu primer servicio

A continuación, vamos a crear nuestro primer servicio, el cual será la tabla de categorías la cual nos permite clasificar a los productos.

Los pasos de forma general para crear un servicio son:

1. Crear una clase con los campos de tu tabla.
2. Agregar la clase al contexto de la base de datos, esta clase contiene todas las tablas de tu base de datos.
3. Agregar una migración para llevar el control de cambios de la base de datos.
4. Actualizar la base de datos con el comando de migración.
5. Generar el controller en base a los campos de tu tabla.
