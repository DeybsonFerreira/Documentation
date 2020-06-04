---
description: 'dicas sobre C#'
---

# C\#

## Receber arquivo 'File' via API 

> Um exemplo de como obtemos um arquivo File, e lemos través do StreamReader, e vemos o resultado do arquivo "ex TXT " em uma string

```csharp
[HttpPost]
public IActionResult Read([FromForm]IFormFile file)
{
    //ler o txt do arquivo >>
    var result = new StringBuilder();
    using (var reader = new StreamReader(file.OpenReadStream()))
    {
        while (reader.Peek() >= 0)
            result.AppendLine(reader.ReadLine());
    }
    result.ToString();
    Return Ok();
 }
```

## Método para adicionar arquivo .txt na pasta do Windows

> Através deste método é possível gerar um arquivo txt, através da string de array

```csharp
string[] lines = {'linha1','linha2','linha3' };

//endereco
string docPath =Environment.GetFolderPath(Environment.SpecialFolder.Desktop);
string fileName="Aarquivo.txt";
//gerar linha por linha
using (System.IO.StreamWriter outputFile = new System.IO.StreamWriter(System.IO.Path.Combine(docPath,fileName)))
{
	foreach (string line in lines)
		outputFile.WriteLine(line);
}
```

## Expressão Lambda

Expressões Lambda são expressões de consulta feitas sobre coleções de dados de forma extremamente otimizada e simples, criando um poderosa ferramenta de produtividade

```csharp
var person1 = personList.Where(x => x.Idade > 35);
var person2 = personList.Select(x => x.Nome== "Deybson").OrderBy(x=>x);
var person3 = personList.Where(x => x.Sobrenome== "Ferreira").ToList();
```

## Serialização para Json 

Com a serialização, você pode transformar uma class de objeto para Json \(String\) e a descerialização, transformar Json, para Classe C\#

```csharp
string json = Newtonsoft.Json.JsonConvert.SerializeObject(variavel);

```

```aspnet
List<Responsible> responsibleList = Newtonsoft.Json.JsonConvert.DeserializeObject<List<Responsible>>(json);
```

## Criando seu próprio JsonResult 

**Obs**: nem sempre, 'tudo' precisa ser exibido para View, por isso é mais prático enviarmos somente o necessário, para melhor otimização/desempenho  

```text
   return Json(new
        {
            PersonId= Guid.NewGuid(),
            Now=DateTime.Now,
            Description="Descrição de teste"
        });
```

## Last Time of the day

```csharp
 public static DateTime LastTime(this DateTime dateTime)
{
    return dateTime.AddTicks(-1).AddDays(1);
}
```

## PadLeft / PadRight

{% tabs %}
{% tab title="PadLeft" %}
```csharp
String Numero="123";
int qtdPosicao=10;
Console.WriteLine(Numero.PadLeft(qtdPosicao,'0')); //0000000123
```
{% endtab %}

{% tab title="PadRight" %}
```csharp
String Numero="123";
int qtdPosicao=10;
Console.WriteLine(Numero.PadRight(qtdPosicao,'0')); //1230000000
```
{% endtab %}
{% endtabs %}

## Convert Date 🕐 

```csharp
  string example="12/30/2019";
  string example="2019/12/30";
  DateTime myDate= Convert.ToDateTime(example);
  
```

## Formato de datas 🕐 

```csharp
DateTime.Now.ToString("yyyy/dd/MM"); // 2019/30/12
DateTime.Now.ToString("dd/NN/yyyy"); // 30/12/2019
```

## Data com hora Universal \( Hora 0 \) 🕐 

```csharp
DateTime.UtcNow; // para usar a data/hora UTC0
DateTime.UtcNow.Date; // para usar somente a Data ( sem horas)
```

## Data real do pais 🕐  

{% code title="C\#" %}
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
{% endcode %}

## Cultura  

> Alterando a cultura

```csharp
string cultureCode="PT-BR";
CultureInfo culture = CultureInfo.GetCultureInfo(cultureCode);
Thread.CurrentThread.CurrentCulture = culture;
Thread.CurrentThread.CurrentUICulture = culture;
```

