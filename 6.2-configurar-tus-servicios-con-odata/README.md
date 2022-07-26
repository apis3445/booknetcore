# 7. Crear servicios con OData

Como se explico en el [capítulo 2](../3.-servicios-rest/) en la explicación de [servicios REST](../3.-servicios-rest/3.1-servicios-rest/) tus servicios pueden filtrar la información o seleccionar solamente algunos campos de una tabla se puede utilizar [OData ](https://www.odata.org)(Open Data Protocol).&#x20;

Las opciones disponibles son:

| Opción                    | Descripción                                                                                                                             |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| $select=clave,nombre      | Seleccionar los campos de la tabla que deseas obtener en el servicio. En este ejemplo solo se seleccionan los campos de clave y nombre. |
| $orderby=clave desc       | Ordenar el resultado por el campo clave de forma descendente                                                                            |
| $filter=clave gt 10       | Permite filtrar los resultados. En este ejemplo se regresan los registros en el cual la clave sea mayor a 1                             |
| $skip=4                   | Permite omitir los primeros 4 registros, lo puedes combinar con $orderby                                                                |
| $top=10                   | Obtiene los primeros 10 registros                                                                                                       |
| $count=true               | Regresa también el total de registros                                                                                                   |
| productos$expand=clientes | Permite además de obtener los productos obtener los datos de los clientes.                                                              |

Puedes ver la documentación de OData con todas las opciones disponibles [aquí](http://docs.oasis-open.org/odata/odata/v4.01/odata-v4.01-part2-url-conventions.html).

Puedes consultar la documentación oficial de Microsoft [aquí](https://docs.microsoft.com/en-us/odata/webapi/first-odata-api).



