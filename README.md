Web-Response
============

Português: Classe para retornar respostas para serviços web com um padrão comum definido  
English: Class to return response to web services with a common pattern  
  
### EM PORTUGUÊS
  
Exemplo em PHP:  
  
> exemplo de sucesso  
  
```php
$response = new WebRespone();
$response->setSuccess(true); 
$response->setMessage('redirect');  
$response->addData('url-to-redirect', 'http://www.prsolucoes.com');
echo($response);
```
  
> exemplo de erro na validação  

```php
$response = new WebRespone();
$response->setSuccess(false);
$response->setMessage('validate');
$response->addError('nome', 'O nome não pode ser vazio');
$response->addError('email', 'O email informado é inválido');
echo($response);
```

> exemplo de erro comum  

```php
$response = new WebRespone();  
$response->setSuccess(false);
$response->setMessage('login-error');
echo($response);
```
