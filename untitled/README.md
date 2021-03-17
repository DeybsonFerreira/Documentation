---
description: 'Tips for javascript, Font-End'
---

# Javascript

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



