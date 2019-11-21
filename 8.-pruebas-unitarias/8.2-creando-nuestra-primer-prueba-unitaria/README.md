# 8.2 Creando nuestra primer prueba unitaria

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

Modificamos nuestro archivo **UnitTest1** para agregar un método que se llame **SumaDosNumeros,** aquí declaramos 2 variables enteras **a** y **b**, la inicializamos con algún valor, 3 y 1 y creamos un nuevo objeto de nuestra clase Operaciones y le pasamos nuestras variables a y b.

Por lo general las pruebas unitarias se componen de 3 partes:

1. **Inicialización de datos:** Aqui cargamos los datos y los objetos de la función que deseamos probar
2. **Método a probar:** Aqui ejecutamos el método que deseamos probar con los datos definidos en la sección anterior
3. **Comprobación del resultado.** Aqui comprobamos el resultado obtenido por la función con el resultado esperado

![](../../.gitbook/assets/image%20%28168%29.png)

Para realizar la prueba se utiliza la instrucción Assert la cual tiene varios métodos como Equal para comparar los valores de 2 variables, True para comprobar algún valor boleano.

En nuestro caso utilizaremos Equal ya que deseamos comparar un valor. Como nuestras variables son 3 y 1 ya sabemos que el valor al sumar estos 2 valores el resultado debe ser 4, entonces en la función Assert el primer párametro es el valor esperado, y el segundo  es la variable regresada por nuestra función Sumar que es el valor que deseamos comprobar

```text
Aseert.Equal(Valor Esperado, Valor Encontrado)
```

{% code title="UnitTest1.cs" %}
```csharp
[Fact]
public void SumaDosNumeros_Correcto()
{
    int a = 3;
    int b = 1;
    Operaciones operaciones = new Operaciones(a,b);
    int resultado = operaciones.Sumar();
    Assert.Equal(4, resultado);
}
```
{% endcode %}





