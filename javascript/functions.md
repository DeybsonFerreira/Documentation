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

## Zero à esquerda

```javascript
function ZeroLeft(str, length) {
    const resto = length - String(str).length;
    return '0'.repeat(resto > 0 ? resto : '0') + str;
}
```

## Verificar se o Evento digitado é Número

```javascript
function isNumber(e) {
    var tecla = (window.event) ? e.keyCode : e.which;
    if ((tecla > 47 && tecla < 58) || tecla == 8 || tecla == 0) {
        return true;
    } else {
        return false;
    }
}


```



