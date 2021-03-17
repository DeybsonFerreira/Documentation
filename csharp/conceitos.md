# Conceitos

## Orientada a Objeto

{% embed url="https://docs.microsoft.com/pt-br/dotnet/csharp/programming-guide/concepts/object-oriented-programming" %}

## Princípio/pilares da Orientação a objeto

**Abstração -** Como __estamos lidando com uma representação de um objeto real

**Encapsulamento -** Se trata de um dos elementos que adicionam segurança à aplicação em uma programação orientada a objetos pelo fato de esconder as propriedades, criando uma espécie de caixa preta.

**Herança -** O reuso de código, capacidade de criar novas classes com base em uma classe existente, aproveitando suas propriedades

**Polimorfismo -**  os objetos filhos herdam as características e ações de seus “ancestrais”. Entretanto, em alguns casos, é necessário que as ações para um mesmo método seja diferente. Em outras palavras, o _polimorfismo_ consiste na alteração do funcionamento interno de um método herdado de um objeto pai.  
`exemplo`: a classe `Eletrodoméstico` possui a função `Ligar();` possuímos duas classes herdada as características do `Eletrodoméstico` , que são: `Televisão, Radio`, \(elas herdam o método `Ligar();` porém ambas ligam de maneiras diferentes.

## Modificadores de acesso

[**`public`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/public)O tipo ou membro pode ser acessado por qualquer outro código no mesmo assembly ou outro assembly que faça referência a ele.

[**`private`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/private) ****O tipo ou membro pode ser acessado apenas por código na mesma classe ou estrutura.

[**`protected`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/protected) ****O tipo ou membro pode ser acessado apenas por código na mesma classe ou estrutura ou em uma classe derivada.

[**`private protected`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/private-protected) \(adicionado em C \# 7.2\) O tipo ou membro pode ser acessado apenas por código na mesma classe ou estrutura ou em uma classe derivada do mesmo assembly, mas não de outro assembly.

[**`internal`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/internal) ****O tipo ou membro pode ser acessado por qualquer código no mesmo assembly, mas não de outro assembly.

[**`protected internal`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/protected-internal) ****O tipo ou membro pode ser acessado por qualquer código no mesmo assembly ou por qualquer classe derivada em outro assembly.

