# Dicas

## **Inicializadores** de Objetos

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

## Como trabalhar com JSON gigante

Esta codificação se aplica quando o volume de informações é muito grande para trafegar do controller para a view.

No controller o retorno do método deve ser conforme abaixo.

```text
return JsonConvert.SerializeObject(new { ParametroRetorno = result });
```

No javascript a function que recebe o retorno deve ser conforme abaixo.

```text
 var retorno = JSON.parse(result).ParametroRetorno;
```

