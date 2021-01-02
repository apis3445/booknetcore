# 1. Introducción

Cuando desarrollamos una app móvil donde se necesita que el usuario guarde información de forma permanente, como por ejemplo una lista de tareas, la información se guarda en una base de datos. Se recomienda que la app no se conecte directamente a la base de datos, si no mediante servicios REST. 

También algunos sistemas Web desarrollados con Angular, React o Vue, la información se obtiene mediante servicios REST.

Este tutorial  explicará paso a paso cómo crear servicios REST con .NET Core con C\# con una sencilla aplicación de ejemplo. 

Aprenderás lo siguiente:

* Como llevar el control de código fuente de tu proyecto con GIT\(manejar en versiones el historial de cambios de tu código\)
* Como manejar versiones de tu base de datos \(mediante migraciones\)
* Entity Framewok para las operaciones de altas, bajas, cambios, lectura \(SQL Server, MySQL\)
* Servicios REST \(con documentación en swagger\)
* Seguridad para tus servicios con OAUTH
* Pruebas unitarias
* Pruebas de integración
* Pruebas de usuario
* Como publicar la aplicación en IIS y en Linux \(Ubuntu\)

Se debe tener conocimientos básicos de C\# y programación orientada a objetos.

### ¿Porqué ASP.NET Core?

ASP.NET Core fue creado para ser multiplataforma \(Windows,Mac,Linux\), open source y con mejoras en rendimiento. Con la versión 5 de .Net se han unificado los 2 framework, el 4.6 y el .Net Core. Puedes ver un artículo mas detallado sobre este cambio [aquí](https://devblogs.microsoft.com/dotnet/introducing-net-5/)

Entity Framework Core también fue rediseñado para hacerlo mas eficiente.

### Requisitos

[Visual Studio Code](https://code.visualstudio.com/download) o V[isual Studio Comunity](https://visualstudio.microsoft.com/es/vs/community/)

[SQL Server Express](https://www.microsoft.com/es-mx/sql-server/sql-server-editions-express) o [MySQL Comunity Version](https://dev.mysql.com/downloads/mysql/)

En este tutorial mostrare ejemplos con Visual Studio Comunity 

Para MySql utilizare [DB Forge for MySQL Express](https://www.devart.com/dbforge/mysql/studio/download.html) y el [MySQLWorkbench](https://dev.mysql.com/downloads/workbench/) 

### Código de ejemplo

El código de ejemplo está en github lo puedes descargar [aquí](https://github.com/apis3445/CaducaRest)

