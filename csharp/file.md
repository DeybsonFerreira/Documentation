---
description: 'Trabalhando com arquivos file C#, aspNet, API'
---

# File

## Arquivo em Byte

> Código C\# para transformar seu arquivo em byte\[\]

```csharp
 string tempPath="C:\Downloads\Arquivo.txt";
 byte[] result = System.IO.File.ReadAllBytes(tempPath); ler bytes de um arquivo
```

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
    string txtString=result.ToString();
    Return Ok(txtString);
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

## Salvar File em uma pasta 

Método para salvar um arquivo/imagem em uma determina pasta do projeto 

```csharp
[HttpPost]
public void SavePicture(HttpPostedFileBase file)
{
    if (file.ContentLength > 0)
    {
        string filename = Path.GetFileName(file.FileName);
        string filepath = Path.Combine(Server.MapPath("~/FilesUpload"),filename);
        file.SaveAs(filepath);
    }
}
```

## Criando Arquivo TXT e Inserindo informações

```csharp
System.IO.File.WriteAllText(AppDomain.CurrentDomain.BaseDirectory + "\\Locale\\Log.txt", "Starting printing");
System.IO.File.CreateText(@"c:\temp\Log.txt").WriteLine("criando parametro 1");
```



