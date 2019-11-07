# 11.3 ¿Qué es Cypress?

Selenium ya tiene varios años en el mercado, actualmente existen otras alternativas que utilizan Javascript y que requieren de node, una opción interesante es Cypress

Puedes agregarlo a tus proyectos de Angular, React, o Vue o puedes descargarlo aquí

{% embed url="https://docs.cypress.io/guides/getting-started/installing-cypress.html\#System-requirements" %}

Una vez instalado puedes realizar tus pruebas en diferentes navegadores

![](../.gitbook/assets/image%20%28200%29.png)

Al igual que selenium te permite abrir tu navegador chrome y seleccionar elmentos, etc

![](../.gitbook/assets/image%20%28125%29.png)

Un ejemplo básico podria ser este, donde abres primero la página de google y luego la de doodles, al darle clic en un archivo se ejecuta la prueba

{% tabs %}
{% tab title="prueba.spec.js" %}
```javascript
/// <reference types="Cypress" />context('Navigation', () => {    beforeEach(() => {        cy.visit('http://www.google.com')    })    it('cy.visit() - visit a remote url', () => {        // https://on.cypress.io/visit        // Visit any sub-domain of your current domain        // Pass options to the visit        cy.visit('https://www.google.com/doodles/', {            timeout: 50000, // increase total time for the visit to resolve            onBeforeLoad(contentWindow) {                // contentWindow is the remote page's window object                expect(typeof contentWindow === 'object').to.be.true            },            onLoad(contentWindow) {                // contentWindow is the remote page's window object                expect(typeof contentWindow === 'object').to.be.true            },        })    })})
```
{% endtab %}
{% endtabs %}

Se muestra el siguiente resultado

![](../.gitbook/assets/image%20%28194%29.png)



