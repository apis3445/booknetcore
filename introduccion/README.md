# 1. Introducción

Cuando desarrollamos una app móvil donde se necesita que el usuario guarde información de forma permanente, como por ejemplo una lista de tareas, por lo general la información se guarda en una base de datos. Se recomienda que la app no se conecte directamente a la base de datos, si no mediante servicios REST.&#x20;

También en los sistemas Web desarrollados con Angular, React o Vue, la información se almacena y se obtiene mediante servicios REST o GraphQL

Este tutorial  explicará paso a paso cómo crear servicios REST con .NET Core (ahora .NET 6) en C# con una aplicación de ejemplo.&#x20;

Aprenderás lo siguiente:

* [Como llevar el control de código fuente de tu proyecto con GIT (manejar en versiones, el historial de cambios de tu código)](../3.-servicios-rest/3.10-git.md)
* [Como manejar versiones de tu base de datos (mediante migraciones)](../3.-servicios-rest/3.1-generar-versiones-de-tu-base-de-datos.md)
* [Entity Framewok para las operaciones de altas, bajas, cambios, consulta (SQL Server, MySQL)](../4.-creando-tu-primer-servicio/4.2-crear-las-tablas.md)
* [Servicios REST (con documentación en swagger)](../3.-servicios-rest/3.1-servicios-rest/)
* [GraphQL](../6.3-agregar-graphql/)&#x20;
* [Seguridad para tus servicios con OAUTH](../7.-seguridad/)
* [Pruebas unitarias](../8.-pruebas-unitarias/)
* [Pruebas de integración](../10.-pruebas-de-integracion/)
* [Pruebas de usuario](../9.-pruebas-de-integracion/)
* [Despliegue continuo con Azure Devops y Azure](../12.-entrega-continua-continuous-delivery/)
* [Como publicar la aplicación en IIS ](../10.-instalacion-en-windows-server-e-iis/16.1-instalar-el-iis-en-windows-server.md)y en [Linux (Ubuntu)](../11.-instalacion-en-linux/)

Se debe tener conocimientos básicos de C# y programación orientada a objetos.

### ¿Porqué ASP.NET Core?

ASP.NET Core fue creado para ser multiplataforma (Windows,Mac,Linux), open source y con mejoras en rendimiento. Con la versión 5 de .Net se han unificado los 2 framework, el 4.6 y el .Net Core. Puedes ver un artículo mas detallado sobre este cambio [aquí](https://devblogs.microsoft.com/dotnet/introducing-net-5/)

Entity Framework Core fue rediseñado para hacerlo mas eficiente.

### Requisitos

[Visual Studio Code](https://code.visualstudio.com/download) o V[isual Studio Comunity](https://visualstudio.microsoft.com/es/vs/community/)

[SQL Server Express](https://www.microsoft.com/es-mx/sql-server/sql-server-editions-express) o [MySQL Comunity Version](https://dev.mysql.com/downloads/mysql/)

En este tutorial mostrare ejemplos con Visual Studio Comunity&#x20;

Para MySql utilizare [DB Forge for MySQL Express](https://www.devart.com/dbforge/mysql/studio/download.html) y [MySQLWorkbench](https://dev.mysql.com/downloads/workbench/)&#x20;

### Código de ejemplo

El código de ejemplo está en github lo puedes descargar [aquí](https://github.com/apis3445/CaducaRest)
