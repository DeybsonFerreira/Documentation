---
description: 'Tips for javascript, FontEnd'
---

# Javascript

## Replace em toda string

> Em javscript, quando demos um replace em uma variável string, ela substitui somente na primeira posição, este código abaixo, verifica em todas as posições fazendo a substituição da string

```javascript
value.replace(/\,/g, "");
```



## Zero à esquerda

```javascript
function ZeroLeft(str, length) {
    const resto = length - String(str).length;
    return '0'.repeat(resto > 0 ? resto : '0') + str;
}
```

