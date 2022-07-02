# 2.1 Servicios REST

Actualmente la mayoría de las empresas como Google, Microsoft, Dropbox, Linkedin, Twitter, permiten a los programadores conectarse a sus servicios mediante servicios REST (**RE**presentational **S**tate **T**ransfer). Estos servicios reciben las peticiones por el protocolo HTTP el cual se usa para ver cualquier página en un navegador web.

Al desarrollar sistemas móviles se recomienda que te conectes mediante servicios REST los cuales manejan toda la lógica de tu aplicación y puede ser consumida por aplicaciones de escritorio o sistemas Web. Esto es debido a que los celulares no tienen tanto poder de procesamiento como lo tiene un servidor.

![ Funcionamiento de servicios rest](<../../.gitbook/assets/image (3).png>)

Los servicios REST te permiten acceder y/o modificar la información mediante los métodos HTTP, por lo cual puedes acceder a ellos mediante URLs. Por lo general regresan la información en formato JSON, aunque también pueden regresar archivos XML o csv. Debido a lo sencillo de desarrollar y consumir actualmente son muy utilizados.

### Archivos JSON

Los archivos JSON (JavaScript Object Notation) son archivos de texto para intercambiar información. La mayoría de los lenguajes de programación como C#, PHP, Java, Android, Swift cuentan con clases para convertir tus objetos en archivos JSON. Los archivos JSON están formados por una clave y un valor o un arreglo de propiedades.&#x20;

Un ejemplo de un archivo JSON el cual contiene información de los países es el siguiente:

```javascript
[
  { 
   "Nombre": "Mexico",
   "Codigo": "MX",
   "Capital": "Mexico City",
   "Moneda": [{
                "Codigo": "MXN",
                "Nombre": "Mexican Peso",
                "Simbolo": "$"}],
   "Bandera": "https://restcountries.eu/data/mex.svg" 
   },
   { 
   "Nombre": "Argentina",
   "Codigo": "AR",
   "Capital": "Buenos Aires",
   "Moneda": [{
                "Codigo": "ARS",
                "Nombre": "Argentine Peso",
                "Simbolo": "$"}],
   "Bandera": "https://restcountries.eu/data/arg.svg" 
   }
]
```

Existen varios servicios públicos los cuales te dan información como por ejemplo del clima, países, películas, libros. Por ejemplo los siguientes servicios te dan información de un país o de acuerdo a una ip saber cual es el país.

* &#x20;[https://restcountries.eu/rest/v2/name/mexico](https://restcountries.eu/rest/v2/name/mexico)  &#x20;
* &#x20;[http://ip-api.com/json](http://ip-api.com/json)

Por lo general para utilizar un servicio de terceros como Microsoft, Google, Twitter te registras y te dan un API Key el cual es como una clave que te asignan para que te conectes a sus servicios, algunos son gratuitos otros tienen costo. Los siguientes servicios te dan información del clima o de una película de acuerdo al Api key o Api Id

* &#x20;[https://samples.openweathermap.org/data/2.5/weather?q=London,uk\&appid=b6907d289e10d714a6e88b30761fae22](https://samples.openweathermap.org/data/2.5/weather?q=London,uk\&appid=b6907d289e10d714a6e88b30761fae22)  &#x20;
* [http://www.omdbapi.com/?t=superman\&apikey=PlzBanM3](http://www.omdbapi.com/?t=superman\&apikey=PlzBanM3)

Los servicios mas comunes son los siguientes:

| Método | Servicio REST                          | Descripción                        |
| ------ | -------------------------------------- | ---------------------------------- |
| GET    |  _http://localhost:5000/_api/Clientes  | Obtiene todos los clientes         |
| GET    |  _http://localhost:5000/_api/Cliente/1 | Obtiene los datos del cliente 1    |
| POST   | _http://localhost:5000/_api/Cliente    | Agrega un nuevo cliente            |
| PUT    | _http://localhost:5000/_api/Cliente/1  | Modifica todos los datos cliente 1 |
| PATCH  | _http://localhost:5000/_api/Cliente/1  | Modifica algunos datos del cliente |
| DELETE | _http://localhost:5000/_api/Cliente/1  | Borra el cliente 1                 |

### **Status Codes (Códigos de Estatus)**

Los servicios REST manejan Códigos de Estatus para indicar empiezan con:

* 200: la acción se realizó correctamente (Succesful)
* 300: se ha tenido que tomar una acción adiconal(Redirección)
* 400: Se esta enviando mal la información al servicio (Errores del cliente)
* 500: el error es de parte del servidor o de quien crea el servicio (Errores del servidor)

#### **Códigos Correctos mas comunes**

| Acción | Código de Estatus | Descripción   |
| ------ | ----------------- | ------------- |
| GET    | 200               | OK            |
| POST   | 201               | Creado        |
| PUT    | 204               | Sin Contenido |
| DELETE | 204               | Sin Contenido |

#### **Códigos de Errores del cliente**

| Código | Nombre                            | Descripción                                                                                                                                                                                                                                                              |
| ------ | --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 400    | Bad Request(Solicitud Incorrecta) | Al consumir el servicio se envía información incorrecta como por ejemplo mandar la palabra 9 años para un campo de edad que espera un número entero.                                                                                                                     |
| 401    | Unauthorized (No Autorizado)      | El servicio requiere que el usuario este identificado.                                                                                                                                                                                                                   |
| 403    | Forbidden (Prohibido)             | El usuario no tiene permiso para realizar la acción. Por ejemplo no tiene permiso para consultar la información.                                                                                                                                                         |
| 404    | Not Found (No Encontrado)         | El contenido a buscar no fue encontrado. Por ejemplo se llama un servicio que no existe o se busca el cliente con Id 20 el cual no existe. Hay debates donde se piensa que si un cliente no existe debe regresar un status 200 con un json vacío o un estatus 400 o 404. |
| 409    | Conflict (Conflicto)              | Por ejemplo estas subiendo un archivo que es anterior al que esta actualmente en el servidor.                                                                                                                                                                            |

#### **Códigos de Errores del servidor**

| Estatus | Nombre                                            | Descripción                                                                                |
| ------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| 500     | Internal Server Error (Error de Servidor Interno) | Por lo general es un error no controlado o inesperado en el servidor                       |
| 503     | Service Unavailable (Servidor No Disponible)      | El servidor no está disponible debido a un mantenimiento por ejemplo que está muy saturado |

Puedes seguir también las recomendaciones de Microsoft en inglés sobre un buen diseño de APIS

{% embed url="https://github.com/microsoft/api-guidelines/blob/vNext/Guidelines.md" %}

### **Filtrar información**&#x20;

Existen opciones adicionales para obtener la información de tus servicios sin tener que estar consultando varios servicios o filtrando la información manualmente, algunas de las principales son ODATA y GraphQL.

