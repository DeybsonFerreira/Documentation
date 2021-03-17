# Funções

## Formatar valor para moeda R$

```javascript
//var value= 100 
//return R$ 100,00
function CurrencyBR(value) {      
    return Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format(value);
}

//outros
function example(value) {

    let options = { style: 'currency', currency: 'USD' };
    console.log(new Intl.NumberFormat('en-US', options).format(value));
    // $1,000,000.50
    console.log(new Intl.NumberFormat('fr-FR', options).format(value));
    // 1 000 000,50 $US
    console.log(new Intl.NumberFormat('in-IN', options).format(value));
    // US$1.000.000,50
    options = { style: 'currency', currency: 'EUR' };
    console.log(new Intl.NumberFormat('en-US', options).format(value));
    // €1,000,000.50
    console.log(new Intl.NumberFormat('fr-FR', options).format(value));
    // 1 000 000,50 €
    console.log(new Intl.NumberFormat('in-IN', options).format(value));
    // €1.000.000,50
}  
```

## Inserir Char no meio da string

Um exemplo para quando temos um número 10000 e quero adicionar um ponto " . " na penúltima casa _decimal, ex "100.00"_ , ou em outra posição.   


```javascript
/**Summary
myString = "100000", = nome da variável em string 
valueToInsert =" . ", = valor que será adicionado 
intPosition =" 2 " = Em qual posição ( traz para frente)
*****/
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

## Somente Números

```javascript
//var mystring="deybson123";
//return 123
function OnlyNumber(mystring) 
{
   mystring= mystring.toString();
   let numsStr = mystring.replace(/[^0-9]/g,'');
   return parseInt(numsStr);
}
```

## Message when exit browser

```javascript
window.onbeforeunload = function(){return "Deseja mesmo sair do site?"};
```

## Aways focus

```javascript
document.hasFocus = function (e) {return true}
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





