---
description: 'dicas sobre C#'
---

# C\#

## Convert Date 🕐 

```csharp
  string example="12/30/2019";
  string example="2019/12/30";
  DateTime myDate= Convert.ToDateTime(example);
  
```

## Formato de datas 🕐 

```csharp
DateTime.Now.ToString("yyyy/dd/MM"); // 2019/30/12
DateTime.Now.ToString("dd/NN/yyyy"); // 30/12/2019
```

## Data com hora Universal \( Hora 0 \) 🕐 

```csharp
DateTime.UtcNow; // para usar a data/hora UTC0
DateTime.UtcNow.Date; // para usar somente a Data ( sem horas)
```

## Data real do pais 🕐  

{% code-tabs %}
{% code-tabs-item title="C\#" %}
```csharp
public DateTime HoraBrasil()
{
    DateTime result =DataTimeZone("Brasilia Standard Time");
    Console.Write(result);
    return result;
}

public DateTime HoraParaguai()
{
    DateTime result = DataTimeZone("Paraguay Standard Time");
    Console.Write(result);
    return result;
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Cultura  

> Alterando a cultura

```csharp
string cultureCode="PT-BR";
CultureInfo culture = CultureInfo.GetCultureInfo(cultureCode);
Thread.CurrentThread.CurrentCulture = culture;
Thread.CurrentThread.CurrentUICulture = culture;
```

## PadLeft / PadRight

{% tabs %}
{% tab title="PadLeft" %}
```csharp
String Numero="123";
int qtdPosicao=10;
Console.WriteLine(Numero.PadLeft(qtdPosicao,'0')); //0000000123
```
{% endtab %}

{% tab title="PadRight" %}
```csharp
String Numero="123";
int qtdPosicao=10;
Console.WriteLine(Numero.PadRight(qtdPosicao,'0')); //1230000000
```
{% endtab %}
{% endtabs %}

