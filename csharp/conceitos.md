# Conceitos

## Modificadores de acesso

[**`public`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/public)O tipo ou membro pode ser acessado por qualquer outro código no mesmo assembly ou outro assembly que faça referência a ele.

[**`private`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/private) ****O tipo ou membro pode ser acessado apenas por código na mesma classe ou estrutura.

[**`protected`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/protected) ****O tipo ou membro pode ser acessado apenas por código na mesma classe ou estrutura ou em uma classe derivada.

[**`private protected`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/private-protected) \(adicionado em C \# 7.2\) O tipo ou membro pode ser acessado apenas por código na mesma classe ou estrutura ou em uma classe derivada do mesmo assembly, mas não de outro assembly.

[**`internal`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/internal) ****O tipo ou membro pode ser acessado por qualquer código no mesmo assembly, mas não de outro assembly.

[**`protected internal`**](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/protected-internal) ****O tipo ou membro pode ser acessado por qualquer código no mesmo assembly ou por qualquer classe derivada em outro assembly.

