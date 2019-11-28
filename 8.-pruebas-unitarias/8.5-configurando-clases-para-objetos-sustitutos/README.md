# 8.5 Configurando Clases para Objetos Sustitutos

Por lo general las pruebas unitarias utilizan objetos sustitutos, para sustituir por ejemplo la base de datos, acceso a algún archivo, servicio rest, por objetos que en realidad no hacen nada, por lo general para realizar este cambio se debe crear una interface, y 2 clases, una clase con los datos reales de acceo a la base de datos, servcios rest, etc y una clase que simula en memoria dicho comportamiento.

Vamos a necesitar los siguientes objetos sustitutos para crear una base de datos en memoria, y otra para simular el objeto para mensajes de error.

1. **CaducaContextMemoria**: Aquí vamos a crear una base de datos en memoria con datos fijos.
2. **MockLocService**: Esta clase va a sustituir los mensajes de error. 



