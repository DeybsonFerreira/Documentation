---
description: 'Lembretes e dicas para API''s , ASP NET , CORE..'
---

# API

## Retornos HTTP's

Códigos de retornos básicos , para mais detalhes \(Referência _****_[_**https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status**_](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status)_**\)**_

```csharp
[HttpGet]
public IActionResult GetExemplo()
{
   return OK();      //200 - Esta requisição foi bem sucedida
   return Created(); //201 - Criado com sucesso
   return NoContent();//204 - Não há nenhum conteúdo
   return NotFound(); //404 - Recurso não encontrado
   return BadRequest(); //400 - o Servidor não poderá continuar o processo por falta/erro no processo

}

[HttpGet]
public IActionResult ReturnCodes()
{
   //exemplos para retorno de códigos
   return StatusCode(StatusCodes.Ok);
   return StatusCode(StatusCodes.NotFound);
   return StatusCode(StatusCodes.Status500InternalServerError);
   
   return StatusCode(500);
   return StatusCode(200);
   return StatusCode(404);
   
   return StatusCode(StatusCodes.Status500InternalServerError, responseObject);
}



```

## Definindo a URL pelo método

Url pode ser definida como   **`URL/GetObject/123`** ou **`URL/GetObject/id?=123`**

```csharp
[HttpGet("GetObject/{Id}")]
public IActionResult GetObject(int Id)
{
    var myObject = this._repository.Get(Id); 
    return Ok(myObject);
}

[HttpGet()]
public IActionResult Get(int Id)
{
    var myObject = this._repository.Get(Id); 
    return Ok(myObject);
}


```

