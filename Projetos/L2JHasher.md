---

---

# L2JHasher

Driver de encriptação de senhas de L2J para usar com Laravel 8.

## Instalação
```
composer require renan-s-oliveira/l2j-hasher
```
Vá em config/app.php

Comentar Illuminate\Hashing\HashServiceProvider::class e adicionar L2JHasher\ServiceProvider\L2JHashServiceProvider::class,
```
//Illuminate\Hashing\HashServiceProvider::class,

L2JHasher\ServiceProvider\L2JHashServiceProvider::class,
```

Vá em config/fortify.php

Trocar
'passwords' => 'users',
por
```
'passwords' => 'accounts',
```
e

'username' => 'email',

por 
```
'username' => 'login',
```


[Tutorial passo a passo, Usando o L2JHasher Laravel 8](https://www.l2jbrasil.com/forums/topic/140933-usando-a-autentica%C3%A7%C3%A3o-do-laravel-8-com-l2jhasher/)

