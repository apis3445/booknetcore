# 3.1 Servicios REST

Actualmente la mayoría de las empresas como Google, Microsoft, Dropbox, Linkedin, Twitter, permiten a los programadores conectarse a sus servicios mediante servicios REST \(**RE**presentational **S**tate **T**ransfer\). Estos servicios reciben las peticiones por el protocolo HTTP el cual se usa para ver cualquier página en un navegador web.

Al desarrollar sistemas móviles se recomienda que te conectes mediante servicios REST los cuales manejan toda la lógica de tu aplicación y puede ser consumida por aplicaciones de escritorio o sistemas Web. Esto es debido a que los celulares no tienen tanto poder de procesamiento como lo tiene un servidor.

![Figura 3.1 Funcionamiento de servicios rest](../../.gitbook/assets/image%20%28341%29.png)

Los servicios REST te permiten acceder y/o modificar la información mediante los métodos HTTP, por lo cual puedes acceder a ellos mediante URL's. Por lo general regresan la información en formato JSON, aunque también pueden regresar archivos XML o csv. Debido a lo sencillo de desarrollar y consumir actualmente muy utilizados

### 3.1.1 Archivos JSON

Los archivos JSON \(JavaScript Object Notation\) son archivos de texto para intercambiar información. La mayoría de los lenguajes de programación como C\#, PHP, Java, Android, Swift cuentan con clases para convertir tus objetos en archivos JSON. Los archivos JSON están formados por una clave y un valor o un arreglo de valores. 

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

Existen varios servicios públicos los cuales te dan información como por ejemplo del clima, países, libros. Por ejemplo los siguientes servicios te dan información de un país o de acuerdo a una ip saber cual es el país.

*  [https://restcountries.eu/rest/v2/name/mexico](https://restcountries.eu/rest/v2/name/mexico)   
*  [http://ip-api.com/json](http://ip-api.com/json)

Por lo general para utilizar un servicio de terceros como Microsoft, Google, Twitter te registras y te dan un API Key el cual es como una clave que te asignan para que te conectes a sus servicios, algunos son gratuitos otros tienen costo. Los siguientes servicios te dan información del clima o de una película de acuerdo al Api key o Api Id

*  [https://samples.openweathermap.org/data/2.5/weather?q=London,uk&appid=b6907d289e10d714a6e88b30761fae22](https://samples.openweathermap.org/data/2.5/weather?q=London,uk&appid=b6907d289e10d714a6e88b30761fae22)   
* [http://www.omdbapi.com/?t=superman&apikey=PlzBanM3](http://www.omdbapi.com/?t=superman&apikey=PlzBanM3)

Los servicios mas comunes son los siguientes:

| Método | Servicio REST | Descripción |
| :--- | :--- | :--- |
| GET |  _http://localhost:5000/_api/Clientes | Obtiene todos los clientes |
| GET |  _http://localhost:5000/_api/Cliente/1 | Obtiene los datos del cliente 1 |
| POST | _http://localhost:5000/_api/Cliente | Agrega un nuevo cliente  |
| PUT | _http://localhost:5000/_api/Cliente/1 | Modifica todos los datos cliente 1 |
| PATCH | _http://localhost:5000/_api/Cliente/1 | Modifica algunos datos del cliente |
| DELETE | _http://localhost:5000/_api/Cliente/1 | Borra el cliente 1 |

### **3.1.2 Status Codes \(Códigos de Estatus\)**

Los servicios REST manejan Códigos de Estatus para indicar si la acción se realizó correctamente empiezan con 200 de lo contrario es un error. Si empiezan con 400 por lo general quien esta consumiendo el servicio esta enviando mal la información y si empieza con 500 el error es de parte del servidor o de quien crea el servicio.

#### **3.1.2.1 Códigos Correctos**

| Acción | Código de Estatus | Descripción |
| :--- | :--- | :--- |
| GET | 200 | OK |
| POST | 201 | Creado |
| PUT | 204 | Sin Contenido |
| DELETE | 204 | Sin Contenido |

#### **3.1.2.2 Códigos de Errores del cliente**

| Código | Nombre | Descripción |
| :--- | :--- | :--- |
| 400 | Bad Request\(Solicitud Incorrecta\) | Al consumir el servicio se envía información incorrecta como por ejemplo mandar la palabra 9 años para un campo de edar que espera un número entero |
| 401 | Unauthorized \(No Autorizado\) | El servicio requiere que el usuario este identificado  |
| 403 | Forbidden \(Prohibido\) | El usuario no tiene permiso para realizar la acción. Por ejemplo no tiene permiso para consultar la información |
| 404 | Not Found \(No Encontrado\) | El contenido a buscar no fue encontrado. Por ejemplo se busca el cliente con Id 20 el cual no existe |
| 409 | Conflict \(Conflicto\) | Por ejemplo estas subiendo un archivo que es anterior al que esta actualmente en el servidor. |

#### **3.1.2.3 Códigos de Errores del servidor**

| Estatus | Nombre | Descripción |
| :--- | :--- | :--- |
| 500 | Internal Server Error \(Error de Servidor Interno\) | Por lo general es un error no controlado o inesperado en el servidor |
| 503 | Service Unavailable \(Servidor No Disponible\) | El servidor no está disponible debido a un mantenimiento ya que está muy saturado |

### **3.1.3 Filtrar información** 

Existen opciones adicionales para obtener la información de tus servicios sin tener que estar consultando varios servicios o filtrando la información manualmente, algunas de las principales son ODATA y GraphQL



