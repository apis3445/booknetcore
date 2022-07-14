# 10.5 Configurando Clases para Objetos Sustitutos

Para poder sustituir nuestas clases reales por objetos mock, en este caso vamos a sustituir la clase de acceso a datos con una base da datos en memoria. Para esta sustitución se debe crear una interface y 2 clases, una clase con los datos reales de acceso a la base de datos, servicios rest, etc y una clase que simula en memoria dicho comportamiento.

Vamos a necesitar los siguientes objetos sustitutos para crear una base de datos en memoria, y otra para simular el objeto para mensajes de error.

1. **CaducaContextMemoria**: Aquí vamos a crear una base de datos en memoria con datos fijos.
2. **MockLocService**: Esta clase va a sustituir los mensajes de error.&#x20;

