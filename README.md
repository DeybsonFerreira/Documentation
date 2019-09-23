# Banco SQL

## Update em Datetime \(horas\)

Adicionar horas, em DateTime existente ex: Data atual + 3 Horas

```
UPDATE Table set MyData=DATEADD(hh, -3, MyData) 
```

{% hint style="danger" %}
Cuidado para Datas que passam de 23:23hrs + ou 00:00 hrs- , pois as datas dd/mm/yyyy podem ser alteradas também.
{% endhint %}

