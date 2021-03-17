---
description: 'dicas sobre C#'
---

# C\#

##  **Inicializadores de objetos**

```csharp
//Ao invés disso
Person myPerson=new Person();
myPerson.Nome="Deybson";
myPerson.Sobrenome="Ferreira";
myPerson.Cargo="Desenvolvedor";

//podemos fazer isso
Person myPerson=new Person()
{
    Nome="Deybson",
    Sobrenome="Ferreira",
    Cargo="Desenvolvedor"
};

```

## Chunk

Método chunk\( pedaço\) é usado para quando uma variável do tipo Lista existir muitos dados, podendo então dividir essa lista em dois, ou mais pedaços 

```csharp
public static IEnumerable<IEnumerable<T>> Chunk<T>(this IEnumerable<T> source, int chunksize)
{
    while (source.Any())
    {
        yield return source.Take(chunksize);
        source = source.Skip(chunksize);
    }
}
```

```csharp
int qtdMaxperItem=2;
List<string> myList=new List<string>();
myList.add("dado 1");
myList.add("dado 2");
myList.add("dado 3");
myList.add("dado 4");
IEnumerable<IEnumerable<string>> myListChunked= Chunk<string>(myList, qtdMaxperItem);
//myListChunked será duas listas com 2 itens (cada)
//
```

## Remover acentos 

```csharp
public static string NoneAccent(this string texto)
{
   if (string.IsNullOrEmpty(texto))
       return String.Empty;

   byte[] bytes = System.Text.Encoding.GetEncoding("iso-8859-8").GetBytes(texto);
   return System.Text.Encoding.UTF8.GetString(bytes);
}
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

