# Cultura

## Alterar Cultura

> Alterando cultura da Thread, da UICulture, e Culture

{% code-tabs %}
{% code-tabs-item title="C\#" %}
```text
string cultureCode="PT-BR";
CultureInfo culture = CultureInfo.GetCultureInfo(cultureCode);
Thread.CurrentThread.CurrentCulture = culture;
Thread.CurrentThread.CurrentUICulture = culture;
```
{% endcode-tabs-item %}
{% endcode-tabs %}

