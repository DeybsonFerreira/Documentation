# Cookies

## Criar Cookie

Exemplo do método para criação de um token

```javascript
function CreateCookie(token, expirationDate) {
    if (expirationDate) {
        document.cookie = `token=${token}; expires=${expirationDate};path=/`;
    } else {
        document.cookie = `token=${token};path=/`;
    }
}
```

## Obter Cookies

```javascript
function GetToken() {
    const cookies = document.cookie;
    if (!cookies) return '';

    return cookies;    
}
```

## Verificar se existe Cookies

Verificar se existe Cookies \( com o exemplo do **Token**\)

```javascript
function HasToken() {
    const cookies = document.cookie;
    if (cookies.indexOf('token') === -1) {
        return false;
    }
    return true;
}
```

## Deletar Cookies

Método para deletar os Cookies \( o método principal **DeleteToken\(\)** \) que foi utilizado para deletar o token dentro do cookies

```javascript
function DeleteCookie(key, path, domain) {
    document.cookie = encodeURIComponent(key) +
        "=; expires=Thu, 01 Jan 1970 00:00:00 GMT" +
        (domain ? "; domain=" + domain : "") +
        (path ? "; path=" + path : "");
}

function DeleteToken() {
    DeleteCookie('token');
}

```

## Verificar Acesso à telas \( com base no cookies\)

```javascript
function AllowPath() {
    const pathName = window.location.pathname;
    if (!HasToken()) {
        if (pathName === '/Home' || $scope.PathName === '/Product' || pathName === '/') {
            return true;
        }
        return false;
    } else {
        return true;
    }
}

```

