# 10.2 Crear una prueba unitaria

Vamos a crear la prueba más básica, para esto vamos a crear una clase llamada Operaciones con un método Sumar

{% code title="Operaciones.cs" %}
```csharp
public class Operaciones
{
    private int _a;
    private int _b;

    public Operaciones(int a, int b)
    {
        this._a = a;
        this._b = b;
    }

    public int Sumar()
    {
        return _a + _b;
    }
}
```
{% endcode %}

Modificamos nuestro archivo **UnitTest1** y lo renombramos a **OperacionesTest** por lo general el nombre es el nombre de la clase que deseas probar mas la palabra Test o puedes omitir el nombre Test ya que al ser un proyecto de test es lógico que sea de prueba.&#x20;

Un buen nombre para los métodos a probar esta formado por lo siguiente:

* **Unidad de trabajo**: Es la funcionalidad que deseas probar, en lugar de probar por métodos es mejor probar la función
* **Condición**: La descripción del caso de prueba
* **Resultado esperado**: El resultado que esperas obtener con los datos proporcionados

Unidad de Trabajo\_Condicion\_ResultadoEsperado

Ejemplo: Si deseas probar por ejemplo el login algunos nombres serían:

* Login\_CredencialesCorrectas\_RegresaTokenValido
* Login\_CredencialesIncorrectas\_RegresaError
* Login\_CincoIntentosIncorrectas\_RegresaUsuarioBloqueado

De esta manera es claro para cualquier persona conocer las reglas de negocio y verificas que se cumplen las reglas de negocio.

Para agregar un método que se llame **Operaciones\_SumaDosNumeros\_RegresaLaSuma,** aquí declaramos 2 variables enteras **a** y **b**, la inicializamos con algún valor, 3 y 1 y creamos un nuevo objeto de nuestra clase Operaciones y le pasamos nuestras variables a y b.

Por lo general las pruebas unitarias se componen de 3 partes:

1. **Inicialización de datos:** Cargamos los datos y los objetos de la función que deseamos probar
2. **Método a probar:** Ejecutamos el método que deseamos probar con los datos definidos en la sección anterior
3. **Comprobación del resultado.** Comprobamos el resultado obtenido por la función con el resultado esperado

![](<../../.gitbook/assets/image (191).png>)

Para realizar la prueba se utiliza la instrucción Assert la cual tiene varios métodos como:

* **Equal** para comparar los valores de 2 variables .
* **True** para comprobar algún valor booleano.

En nuestro caso utilizaremos Equal ya que deseamos comparar un valor. Como nuestras variables son 3 y 1 ya sabemos que el valor al sumar estos 2 valores el resultado debe ser 4, entonces en la función Assert el primer parámetro es el valor esperado, y el segundo  es la variable regresada por nuestra función Sumar que es el valor que deseamos comprobar

```csharp
Assert.Equal(Valor Esperado, Valor Encontrado)
```

{% code title="OperaciontesTest.cs" %}
```csharp
[Fact]
public void Operaciones_SumaDosNumeros_RegresaLaSuma()
{
    //Inicialización de datos (Arrange)
    int a = 3;
    int b = 1;   
    Operaciones operaciones = new Operaciones(a,b);
    //Método a probar (Act)
    int resultado = operaciones.Sumar();
    //Comprobación de resultados (Assert)
    Assert.Equal(4, resultado);
}
```
{% endcode %}



