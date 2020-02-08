# 10.5.4 Agregando diferentes parámetros con MSTest

Con MSTest puedes pasarle varios parámetros a tu prueba unitaria para no estar repitiendo el mismo código varias veces si solo va a cambiar los parámetros. Pones como atributo DataRow y entre paréntesis agregas los parámetros que deseas pasar.

Para este ejemplo utilizaré el mismo ejemplo de las pruebas unitarias de la clase Operaciones.

Copie la clase operaciones al proyecto CaducaRest.IntegrationTest

Agrega un nuevo archivo de pruebas llamada **PruebasOperaciones**, puedes agregar 2 DataRows, los parámetros será el valor a, el valor b y el resultado.

{% tabs %}
{% tab title="PruebasOperaciones.cs" %}
```csharp
[TestClass]
public class PruebasOperaciones
{
    [TestMethod]
    [DataRow(1,3,4)]
    [DataRow(-2,7,5)]
    public void SumaDosNumeros_Correcto(int a, int b, int total)
    {
        Operaciones operaciones = new Operaciones(a, b);
        int resultado = operaciones.Sumar();
        Assert.AreEqual(total, resultado);
    }
}
```
{% endtab %}
{% endtabs %}

Puedes ver la documentación oficial aquí

{% embed url="https://docs.microsoft.com/es-mx/dotnet/core/testing/unit-testing-with-mstest" %}



