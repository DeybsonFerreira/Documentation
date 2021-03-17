---
description: 'trabalhando com Json em C#'
---

# Json

## Serialização e Desserialização  

Com a serialização, você pode transformar uma class de objeto para Json \(String\) e a descerialização, transformar Json, para Classe C\#

```csharp
/*********************Serialize**********************************/
string json = Newtonsoft.Json.JsonConvert.SerializeObject(variavel);

/*********************Deserialize**********************************/
List<Responsible> responsibleList = Newtonsoft.Json.JsonConvert.DeserializeObject<List<Responsible>>(json);


```

## Criando seu próprio JsonResult 

**Obs**: nem sempre, 'tudo' precisa ser exibido para View, por isso é mais prático enviarmos somente o necessário, para melhor otimização/desempenho  

```csharp
   /************ Serializando com Json *******************************/
   var myJson=new JsonResult(new {PersonId=Guid.NewGuid()},Message="Exemplo")
   return Ok(myJson);

   //ou criando o Json
   
   return Json(new
                {
                    PersonId= Guid.NewGuid(),
                    Now=DateTime.Now,
                    Description="Descrição de teste"
                });
```

