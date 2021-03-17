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

## Outras Funções Linq

```csharp
/**************** DADOS *********************************/

var alunos=new List<Aluno>();
alunos.Add(new Aluno(){Id=0, Nome="Deybson",Idade=25});
alunos.Add(new Aluno(){Id=1, Nome="João",Idade=26});
alunos.Add(new Aluno(){Id=2, Nome="Pedro",Idade=27});
alunos.Add(new Aluno(){Id=3, Nome="José",Idade=28});
alunos.Add(new Aluno(){Id=4, Nome="Mateus",Idade=10});

/****************Funções ********************************/
var maiorIdade=alunos.Max(q=>q.Idade);  
var menorIdade=alunos.Min(q=>q.Idade); 
var todasIdades=alunos.Select(q=>q.Idade); 
var menorDeIdade=alunos.Where(q=>q.Idade < 18); 
var somarIdades=alunos.Sum(q=>q.Idade); 
var pegar2Primeiros=alunos.Take(2); 
var pular2Primeiros=alunos.Skip(2); 
var mediaDeIdades=alunos.Average(x=>x.Idade); 

/********* primeiros*********************/
var primeiroDaLsta0=alunos.First(); 
var primeiroDaLsta1=alunos.FirstOrDefault(); 
var primeiroDaLsta2=alunos.Single(); 
var primeiroDaLsta3=alunos.SingleOrDefault(); 


```

