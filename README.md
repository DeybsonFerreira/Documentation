# Banco SQL

##  **DDL ou DML** ❓ 

**DDL =** Data Definition Language &gt; CREATE, o ALTER e o DROP. \( não interagem com os dados e sim com os objetos\)

**DML** = Data Manipulation Language &gt; INSERT, UPDATE e DELETE. \( interagem com os dados\)



## Interação Fech

{% hint style="success" %}
Função equivalente ao Take/Split
{% endhint %}

```sql
--(int) IQtd , ponteiro , a partir de onde, qual posição.

SELECT *
FROM TableExample
ORDER BY TableExampleId
OFFSET (IQtd) ROWS FETCH NEXT (totalResult) ROWS ONLY
```

## Update em Datetime \(horas\)

Adicionar horas, em DateTime existente ex: Data atual + 3 Horas

```sql
UPDATE Table set MyData=DATEADD(hh, -3, MyData) 
```

{% hint style="danger" %}
Cuidado para Datas com horas iniciais ou finais, pois podem ser alterado os dias
{% endhint %}

```sql
@initTime time(2) = '23:59:59.999'; -- Hora +1 será adicionado um novo dia 
@endTime time(2) = '00:00:00.000'; --Hora -1 será voltado o dia
```

## Merge duas tabelas

```sql

MERGE Locality L
    USING Locality2 L2
ON (L.localityId = L2.LocalityId)

WHEN MATCHED
    THEN UPDATE SET 
       L.LocalityTypeId=L2.LocalityTypeId, 
	   L.Code=L2.Code,
	   L.Name=L2.Name,
	   L.Abbreviation=L2.Abbreviation,
	   L.FormattedName=L2.FormattedName,
	   L.ParentId=L2.ParentId 
WHEN NOT MATCHED BY TARGET 
    THEN INSERT (LocalityId,LocalityTypeId,Code,Name,Abbreviation,FormattedName,ParentId)
         VALUES (L2.LocalityId,L2.LocalityTypeId,L2.Code,L2.Name,L2.Abbreviation,L2.FormattedName,L2.ParentId)

		 OUTPUT
   $action,
   inserted.*,
   deleted.*;



```

