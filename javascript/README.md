---
description: 'Tips for javascript, Font-End'
---

# Javascript

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
```

{% page-ref page="./" %}

{% page-ref page="functions.md" %}

{% page-ref page="cookies.md" %}





