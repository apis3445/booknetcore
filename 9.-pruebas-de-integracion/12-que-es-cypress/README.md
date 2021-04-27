# 14.3 ¿Qué es Cypress?

Selenium ya tiene varios años en el mercado, y han surgido nuevas opciones para realizar tus pruebas con javascript/typescript, con algunas mejoras como ya no programar los waits y poder remplazar las respuestas de los servicios con los valores y status code que desees.

Puedes agregarlo a tus proyectos de Angular, React, o Vue o puedes descargarlo en:

{% embed url="https://docs.cypress.io/guides/getting-started/installing-cypress.html\#System-requirements" %}

Una vez instalado puedes realizar tus pruebas en diferentes navegadores

![](../../.gitbook/assets/image%20%28308%29.png)

Al igual que selenium te permite abrir tu navegador chrome y seleccionar elementos, etc

![](../../.gitbook/assets/image%20%28202%29.png)

Un ejemplo básico podría ser este, donde abres primero la página de google y luego la de doodles, al darle clic en un archivo se ejecuta la prueba

{% tabs %}
{% tab title="prueba.spec.js" %}
```javascript
/// <reference types="Cypress" />

context('Navigation', () => {
    beforeEach(() => {
        cy.visit('http://www.google.com')
    })

    it('cy.visit() - visit a remote url', () => {

        // Pass options to the visit
        cy.visit('https://www.google.com/doodles/', {
            timeout: 50000, // increase total time for the visit to resolve
            onBeforeLoad(contentWindow) {
                // contentWindow is the remote page's window object
                expect(typeof contentWindow === 'object').to.be.true
            },
            onLoad(contentWindow) {
                // contentWindow is the remote page's window object
                expect(typeof contentWindow === 'object').to.be.true
            },
        })
    })
})

```
{% endtab %}
{% endtabs %}

Se muestra el siguiente resultado

![](../../.gitbook/assets/image%20%28294%29.png)

Ventajas:

* Detecta cuando se ejecuta un servicio rest, por lo cual ya no debes poner esperas en lo que se completa la llamada sl servicio REST.
* Puedes simular la llamada al servicio rest y sustituir la respuesta por datos fijos.
* También por medio de líneas de comandos te corre las pruebas te graba videos de los test y toma screenshots de los casos de prueba que fallaron.
* Al igual que selenium puedes grabar los pasos y te genera el código.

Desventajas:

* No soportará test con múltiples Tabs e IFrames, aunque se pueden probar con algunos trucos
* De momento no soporta Safari
* No soportará test con múltiples navegadores  Puedes ver la lisa completa aquí [https://docs.cypress.io/guides/references/trade-offs\#Inside-the-browser](https://docs.cypress.io/guides/references/trade-offs#Inside-the-browser)

