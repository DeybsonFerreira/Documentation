---
description: 'Tips for javascript, FontEnd'
---

# Javascript

## Zero à esquerda

```javascript
function ZeroLeft(str, length) {
    const resto = length - String(str).length;
    return '0'.repeat(resto > 0 ? resto : '0') + str;
}
```

