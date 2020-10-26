---
description: 'Tips for javascript, Font-End'
---

# Javascript

## Inserir char no meio da string

> Um exemplo para quando temos um número 10000 e quero adicionar um ponto " . " na penúltima casa decimal, ex "100.00" , ou em outra posição.
>
> **myString** = "100000",  = nome da variável em string  
> **valueToInsert** ="  . ",    = valor que será adicionado   
>  **intPosition** ="  2 "        =  Em qual posição \( traz para frente\)

>

```javascript
function InsertOnString(myString, valueToInsert, intPosition) {

    myString = myString.toString();
    valueToInsert = valueToInsert.toString();
    if (myString.toString().length > intPosition) {

        var initialStr = myString.substring(0, myString.length - intPosition);
        var finalStr = myString.substring(myString.length - intPosition);
        var addingValue = initialStr + valueToInsert + finalStr;
        return addingValue;
    }
    return myString;
}
```

## Formatar valor para moeda R$

```javascript
function FormatMoneyRS(valueString) {
    valueString=parseFloat(valueString);
    valueString = valueString.toFixed(2).toString().replace('.', ','); //inserir virgula
    var valueformated = "0";
    if (valueString.toString().length > 6) {
        valueformated = InsertOnString(valueString.toString(), ".", 6);//inserir ponto de milhar
    }
    return valueformated;
}    
```

## Replace em toda string

> Em javscript, quando demos um replace em uma variável string, ela substitui somente na primeira posição, este código abaixo, verifica em todas as posições fazendo a substituição da string

```javascript
value.replace(/\,/g, "");
```

## Pegar elemento da string , à partir da posição

```javascript
var meuNome="DeybsonFerreira"
var char= meuNome.charAt(7);
//result = F
//D =0 , e=1 ,.....
```

## Zero à esquerda

```javascript
function ZeroLeft(str, length) {
    const resto = length - String(str).length;
    return '0'.repeat(resto > 0 ? resto : '0') + str;
}
```



