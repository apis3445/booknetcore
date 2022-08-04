# 14.3 ¿Qué es Cypress?

Selenium ya tiene varios años y nos ofrece muchas ventajas para los nuevos framework javascript. Con los framework de javascript  ya no tienes que programar los waits y puedes remplazar las respuestas de los servicios con los valores y status code que desees.

Uno de los framework que esta ganando popularidad y mas actualizaciones es Cypress.

Puedes agregarlo a tus proyectos de Angular, React, o Vue o puedes descargarlo en:

{% embed url="https://docs.cypress.io/guides/getting-started/installing-cypress.html#System-requirements" %}

Para correr las pruebas en cypress puedes teclear el comando

```
npx cypress open
```

Te abre la ventana de cypress donde te pregunta si deseas ver los ejemplos. La ventana cuenta con 2 opciones principales:

* Tus archivos de pruebas (pueden ser javascript o typescript)
* El navegador en el que vas a correr las pruebas en este caso Chrome 91

![](<../../.gitbook/assets/image (609).png>)

Al igual que selenium te permite abrir tu navegador chrome y seleccionar elementos, etc

![](<../../.gitbook/assets/image (279).png>)

### Ejemplo

Un ejemplo básico podría ser este, donde abres primero la página de google y luego la de doodles, al darle clic en un archivo se ejecuta la prueba

{% tabs %}
{% tab title="ejemplo.ts" %}
```javascript
/// <reference types="Cypress" />

context('Navigation', () => {
    beforeEach(() => {
        cy.visit('http://www.google.com')
    })

    it('Revisa logo en la pàgina de google', () => {
        // Navega a la pàgina de google doodless
        cy.visit('https://www.google.com/');
        cy.get('.lnXdpd').should('have.attr', 'alt', 'Google')
      
    })
})

```
{% endtab %}
{% endtabs %}

Se muestra el siguiente resultado

![](<../../.gitbook/assets/image (610).png>)

### Ventajas y Desventajas

Ventajas:

* Detecta cuando se ejecuta un servicio rest, por lo cual ya no debes poner esperas en lo que se completa la llamada al servicio REST.
* Puedes simular la llamada al servicio rest y sustituir la respuesta por datos fijos.
* También por medio de líneas de comandos te corre las pruebas, te graba videos de los test y toma screenshots de los casos de prueba que fallaron.
* Al igual que selenium puedes grabar los pasos y te genera el código.

Desventajas:

* No soportará test con múltiples Tabs e IFrames, aunque se pueden probar con algunos paquetes.
* De momento no soporta Safari.
* No soportará test con múltiples navegadores al mismo tiempo.\
  \
  Puedes ver la lisa completa aquí\
  [https://docs.cypress.io/guides/references/trade-offs#Inside-the-browser](https://docs.cypress.io/guides/references/trade-offs#Inside-the-browser)
