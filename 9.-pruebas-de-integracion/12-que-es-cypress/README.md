# 11.3 ¿Qué es Cypress?

Selenium ya tiene varios años en el mercado, actualmente existen otras alternativas que utilizan Javascript , una opción interesante es Cypress

Puedes agregarlo a tus proyectos de Angular, React, o Vue o puedes descargarlo aquí

{% embed url="https://docs.cypress.io/guides/getting-started/installing-cypress.html\#System-requirements" %}

Una vez instalado puedes realizar tus pruebas en diferentes navegadores

![](../../.gitbook/assets/image%20%28268%29.png)

Al igual que selenium te permite abrir tu navegador chrome y seleccionar elmentos, etc

![](../../.gitbook/assets/image%20%28178%29.png)

Un ejemplo básico podria ser este, donde abres primero la página de google y luego la de doodles, al darle clic en un archivo se ejecuta la prueba

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

![](../../.gitbook/assets/image%20%28258%29.png)

Otra de las ventajas que tiene cypress es que detecta cuando se ejecuta un servicio rest, por lo cual ya no debes poner esperas de 5 segundos en lo que se hace la llamada sl servicio REST.

Otra de las ventajas es que puedes simular la llamada al servicio rest y sustituir la respuesta por datos fijos.

También por medio de líneas de comandos te corre las pruebas te graba videos de los test y toma screenshots de los casos de prueba que fallaron.

