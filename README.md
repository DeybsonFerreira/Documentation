# Banco SQL

## Update em Datetime \(horas\)

Adicionar horas, em DateTime existente ex: Data atual + 3 Horas

```sql
UPDATE Table set MyData=DATEADD(hh, -3, MyData) 
```

{% hint style="danger" %}
Cuidado para Datas com horas iniciais ou finais, pois podem ser alterado os dias
{% endhint %}

```text
@initTime time(2) = '23:59:59.999'; -- Hora +1 será adicionado um novo dia 
@endTime time(2) = '00:00:00.000'; --Hora -1 será voltado o dia
```

