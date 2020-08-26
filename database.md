---
description: 'Dicas Banco de dados  , SQL Server'
---

# Banco de dados

## **DDL ou DML** ❓

**DDL =** Data Definition Language &gt; CREATE, o ALTER e o DROP. \( não interagem com os dados e sim com os objetos\)

**DML** = Data Manipulation Language &gt; INSERT, UPDATE e DELETE. \( interagem com os dados\)

## Verificar informações da database

```sql
//INFORMAÇÕES SOBRE O ESPAÇO DO BANCO
Use SeuBanco;
Exec SP_SpaceUsed;
//database_size, unallocated space, reserved, data, index_size, unused


//INFORMAÇÕES DA TABELA
sp_help nome_da_tabela

```

## Interação em consulta

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

{% hint style="warning" %}
Cuidado para Datas com horas iniciais ou finais, pois podem ser alterado os dias
{% endhint %}

```sql
@initTime time(2) = '23:59:59.999'; -- Hora +1 será adicionado um novo dia 
@endTime time(2) = '00:00:00.000'; --Hora -1 será voltado o dia
```

## Merge, Duas Tabelas

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

## SQL - Guid UniqueIdentifier

Para gerar um **guid** aleatório na **primary key** do tipo **UniqueIdentifier**: exemplo:

```sql
CREATE TABLE Usuario(
	Id UNIQUEIDENTIFIER PRIMARY KEY DEFAULT newsequentialid(), // PARA GERAR UM GUID ALEATÓRIO COMO PRIMARY KEY
	Nome varchar(255) NOT NULL ,
	Nascimento Date,
	Telefone varchar(255) NOT NULL,
	Cpf varchar(255) ,
	Rg varchar(255) ,
	img varchar(max)
);
```

