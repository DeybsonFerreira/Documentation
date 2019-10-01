---
description: dicas para datas
---

# DateTime

## Formato de datas

```text
DateTime.Now.ToString("yyyy/dd/mm"); // 2019/30/12
DateTime.Now.ToString("dd/mm/yyyy"); // 30/12/2019
```

## Data com hora Universal \( Hora 0 \)

```text
DateTime.UtcNow;
```

## Data real do pais 

{% code-tabs %}
{% code-tabs-item title="C\#" %}
```text
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
