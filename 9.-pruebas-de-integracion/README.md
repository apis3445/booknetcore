# 14. Pruebas de usuario

Podemos realizar pruebas simulando las accciones que realizaría un usuario como dar clic a un botón y teclear información. Estas pruebas se conocen como E2E Testing.

Como estas pruebas son mas tardadas se suelen solo probar las funciones claves y mas importantes.

&#x20;Una de las opcionees mas utilizadas es [Selenium](https://www.seleniumhq.org)

Existen otras herramientas  para realizar pruebas de tu aplicación web, de escritorio y las aplicaciones móviles, como por ejemplo AppCenter para aplicaciones móviles o Appium para aplicaciones de escritorio.

Otro frameworks interesantes son:\
[\
Cypress](https://www.cypress.io) Puedes realizar tus pruebas con javascript o typescript y no esta basado en selenium.\
[WebDriver.io](https://webdriver.io) Puedes realizar pruebas web o móviles con javascript.\
[Playwrigth](https://playwright.dev) Desarrollado por Microsoft puedes realizar tus pruebas con javascript, typescript, python, java o c#

En general en este tipo de pruebas accedes a los componentes de una página mediante un selector el cual puede ser el Id, la clase css, por medio del texto, entre otros y vas realizando las acciones que hace un usuario como teclear su usuario en la página de login.&#x20;

Puedes realizar el mismo test con los diferentes navegadores y puedes emular el navegador como si fuera un celular.&#x20;

