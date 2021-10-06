---
description: 'List, IList, IEnumerable'
---

# Coleções .NET Framework

### Coleções no .NET Framework

No .NET Framework, temos várias formas de trabalhar com coleções, e muitas vezes ficamos em dúvida sobre qual utilizar ou simplesmente utilizamos List. Portanto, gostaria de apresentar alguns pontos sobre este assunto.

#### Heranças <a id="user-content-heran%C3%A7as"></a>

Vamos observar a cadeia de herança da classe List:

![](../.gitbook/assets/image%20%2819%29.png)

Sempre é mais interessante utilizarmos o objeto primitivo, por ele ser mais simples e implicar num uso menor de memória. Porém, as vezes necessitamos de algum método mais especializado que somente outra classe mais complexa possui. Por isso, é importante entender exatamente o que desejamos fazer, para saber qual objeto atende melhor.

### Qual Devo Utilizar ?

#### IEnumerable&lt;T&gt; <a id="user-content-ienumerable%3Ct%3E"></a>

* Iterar uma coleção, como um `foreach`
* Executar várias operações Lambda
* Sem adicionar ou remover items.

#### ICollection&lt;T&gt; <a id="user-content-icollection%3Ct%3E"></a>

* Iterar uma coleção, como um `foreach`
* Executar várias operações Lambda
* Adicionar ou remover itens dinamicamente.

#### IList&lt;T&gt; <a id="user-content-ilist%3Ct%3E"></a>

* Iterar uma coleção, como um `foreach`
* Executar várias operações Lambda
* Adicionar ou remover itens dinamicamente.
* Manipular itens pelo índice \(`list[i]`\)

#### List&lt;T&gt; <a id="user-content-list%3Ct%3E"></a>

* Iterar uma coleção, como um `foreach`
* Executar várias operações Lambda
* Adicionar ou remover itens dinamicamente.
* Manipular itens pelo índice \(`list[i]`\)
* Manipulações mais complexas, como busca, ordenação e comparação.

### Comparando <a id="user-content-comparando"></a>

Abaixo temos uma tabela listando todas as propriedades e métodos destes 4 objetos, realçando assim suas diferenças:

|  | [IEnumerable&lt;T&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1)  | [ICollection&lt;T&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.icollection-1)  | [IList&lt;T&gt;](https://docs.microsoft.com/pt-br/dotnet/api/system.collections.generic.ilist-1)  | [List&lt;T&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1)  |
| :--- | :--- | :--- | :--- | :--- |
| **Descrição** | Expõe um enumerador, o qual suporta uma simples iteração em uma coleção de um tipo especificado. | Define métodos para manipular coleções genéricas. | Representa uma coleção de objetos que podem ser individualmente acessador pelo índice. | Representa uma lista fortemente tipada que pode ser acessada pelo índice. Fornece métodos para pesquisar, ordenar e manipular listas. |
| --- | --- | --- | --- | --- |
| **Propriedades** |  | Count | Count | Count |
|  |  | IsReadOnly | IsReadOnly | IsReadOnly |
|  |  |  | Item\[Int32\] | Item\[Int32\] |
|  |  |  |  | Capacity |
| --- | --- | --- | --- | --- |
| **Métodos** | GetEnumerator\(\) | GetEnumerator\(\) | GetEnumerator\(\) | GetEnumerator\(\) |
|  |  | Add\(T\) | Add\(T\) | Add\(T\) |
|  |  | Clear\(\) | Clear\(\) | Clear\(\) |
|  |  | Contains\(T\) | Contains\(T\) | Contains\(T\) |
|  |  | CopyTo\(T\[\], Int32\) | CopyTo\(T\[\], Int32\) | CopyTo\(T\[\], Int32\) |
|  |  | Remove\(T\) | Remove\(T\) | Remove\(T\) |
|  |  |  | IndexOf\(T\) | IndexOf\(T\) |
|  |  |  | Insert\(Int32, T\) | Insert\(Int32, T\) |
|  |  |  | RemoveAt\(Int32\) | RemoveAt\(Int32\) |
|  |  |  |  | AddRange\(IEnumerable&lt;T&gt;\) |
|  |  |  |  | AsReadOnly\(\) |
|  |  |  |  | BinarySearch\(Int32, Int32, T, IComparer&lt;T&gt;\) |
|  |  |  |  | BinarySearch\(T\) |
|  |  |  |  | BinarySearch\(T, IComparer&lt;T&gt;\) |
|  |  |  |  | ConvertAll&lt;TOutput&gt;\(Converter&lt;T,TOutput&gt;\) |
|  |  |  |  | CopyTo\(Int32, T\[\], Int32, Int32\) |
|  |  |  |  | CopyTo\(T\[\]\) |
|  |  |  |  | Equals\(Object\) |
|  |  |  |  | Exists\(Predicate&lt;T&gt;\) |
|  |  |  |  | Find\(Predicate&lt;T&gt;\) |
|  |  |  |  | FindAll\(Predicate&lt;T&gt;\) |
|  |  |  |  | FindIndex\(Int32, Int32, Predicate&lt;T&gt;\) |
|  |  |  |  | FindIndex\(Int32, Predicate&lt;T&gt;\) |
|  |  |  |  | FindIndex\(Predicate&lt;T&gt;\) |
|  |  |  |  | FindLast\(Predicate&lt;T&gt;\) |
|  |  |  |  | FindLastIndex\(Int32, Int32, Predicate&lt;T&gt;\) |
|  |  |  |  | FindLastIndex\(Int32, Predicate&lt;T&gt;\) |
|  |  |  |  | FindLastIndex\(Predicate&lt;T&gt;\) |
|  |  |  |  | ForEach\(Action&lt;T&gt;\) |
|  |  |  |  | GetEnumerator\(\) |
|  |  |  |  | GetHashCode\(\) |
|  |  |  |  | GetRange\(Int32, Int32\) |
|  |  |  |  | GetType\(\) |
|  |  |  |  | IndexOf\(T, Int32\) |
|  |  |  |  | IndexOf\(T, Int32, Int32\) |
|  |  |  |  | InsertRange\(Int32, IEnumerable&lt;T&gt;\) |
|  |  |  |  | LastIndexOf\(T\) |
|  |  |  |  | LastIndexOf\(T, Int32\) |
|  |  |  |  | LastIndexOf\(T, Int32, Int32\) |
|  |  |  |  | MemberwiseClone\(\) |
|  |  |  |  | RemoveAll\(Predicate&lt;T&gt;\) |
|  |  |  |  | RemoveRange\(Int32, Int32\) |
|  |  |  |  | Reverse\(\) |
|  |  |  |  | Reverse\(Int32, Int32\) |
|  |  |  |  | Sort\(\) |
|  |  |  |  | Sort\(Comparison&lt;T&gt;\) |
|  |  |  |  | Sort\(IComparer&lt;T&gt;\) |
|  |  |  |  | Sort\(Int32, Int32, IComparer&lt;T&gt;\) |
|  |  |  |  | ToArray\(\) |
|  |  |  |  | ToString\(\) |
|  |  |  |  | TrimExcess\(\) |
|  |  |  |  | TrueForAll\(Predicate&lt;T&gt;\) |

### Fonte <a id="user-content-fonte"></a>

[https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic)   


