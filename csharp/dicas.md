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

