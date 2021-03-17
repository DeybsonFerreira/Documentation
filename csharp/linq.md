---
description: Language Integrated Query
---

# Linq

## Filtros

Expressões Lambda são expressões de consulta feitas sobre coleções de dados de forma extremamente otimizada e simples, criando um poderosa ferramenta de produtividade

```csharp
using System.Linq;

var person1 = personList.Where(x => x.Idade > 35);
var person2 = personList.Select(x => x.Nome== "Deybson").OrderBy(x=>x);
var person3 = personList.Where(x => x.Sobrenome== "Ferreira").ToList();
var person4 = personList.FirstOrDefault(x => x.Nome== "Deybson").OrderBy(x=>x);

bool condition1=idade>=18?"Maior de idade":"Menor de idade";

```

