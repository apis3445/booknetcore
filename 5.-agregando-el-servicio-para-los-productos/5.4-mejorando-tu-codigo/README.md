# 5.5 Validar Reglas Mejorando tu código

Si observamos el código de nuestras clases DAO de Categorías y Productos, es bastante similar, por lo cual lo podemos mejorar creando una única clase genérica con los métodos comunes como obtener todos los registros, obtener un registro por su id, insertar, modificar y borrar un registro, esta clase recibirá como parámetro nuestra clase para la tabla. Este concepto se llama **Generics**

También vamos aprovechar una característica llamada **Filtros** (Filters) para tener una excepción genérica a todos los servicios de una forma sencilla. &#x20;

Los filtros nos permiten definir métodos que se pueden ejecutar:

* Antes de iniciar los métodos de los servicios, para validar que el usuario tiene permiso para acceder a una información.
* Al finalizar un método para registrar el historial de quien agrega o modifica la información.
* Como excepciones para controlar los errores en los servicios





