---
description: Comandos básicos do dotnet
---

# CLI

{% embed url="https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet" caption="Referência \( Microsoft \)" %}

### Versão atual

```aspnet
dotnet --version 
```

### Setando outra versão

```aspnet
dotnet new globaljson --sdk-version 3.0.100 //exemplo 3.0.1
```

### Versões instaladas

```aspnet
dotnet --list-sdks
dotnet --list-runtimes
```

### Lista de Templates

```aspnet
dotnet new
```

### Novo Projeto &gt; escolher o template

```aspnet
dotnet new webapp -n siteExemplo
```

### Executar Testes

```aspnet
dotnet test
```

### Executar projeto

```aspnet
dotnet run 
```

