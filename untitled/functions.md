# Functions

## Only number from string

```javascript
function justNumbers(string) 
{
   let numsStr = string.replace(/[^0-9]/g,'');
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







