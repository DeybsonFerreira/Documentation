---
description: dicas para datas
---

# DateTime

## Convert Date

```csharp
  string example="30/12/2019";
  string example="12/30/2019";
  string example="2019/12/30";
  DateTime myDate= Convert.ToDateTime(example);
```

## Formato de datas

```csharp
DateTime.Now.ToString("yyyy/dd/mm"); // 2019/30/12
DateTime.Now.ToString("dd/mm/yyyy"); // 30/12/2019
```

## Data com hora Universal \( Hora 0 \)

```csharp
DateTime.UtcNow; // para usar a data/hora UTC0
DateTime.UtcNow.Date; // para usar somente a Data ( sem horas)
```

## Data real do pais 

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

