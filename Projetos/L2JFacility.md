---

---

# L2JFacility

Um pacote cheio de métodos para te ajudar a criar sistemas/sites para seu L2J 

## Github

[Github](https://github.com/renan-s-oliveira/l2jfacility)

## Instalação

[English](https://github.com/renan-s-oliveira/l2jfacility/blob/main/README-english.MD)

```
composer require renan-s-oliveira/l2j-facility

php artisan vendor:publish --provider="vendor\renan-s-oliveira\L2JFacilityServiceProvider" --force
```

```

Remover do .env 

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=

Adicionar no .env

DB_CONNECTION=login_server 
DB_HOST_LOGIN=127.0.0.1
DB_PORT_LOGIN=3306
DB_DATABASE_LOGIN=db_name_login
DB_USERNAME_LOGIN=root
DB_PASSWORD_LOGIN=

DB_HOST_GAME_SERVER=127.0.0.1
DB_PORT_GAME_SERVER=3306
DB_DATABASE_GAME_SERVER=db_name_game_server
DB_USERNAME_GAME_SERVER=root
DB_PASSWORD_GAME_SERVER=
```

## Como usar

[English](https://github.com/renan-s-oliveira/l2jfacility/blob/main/src/usage/english/ENGLISH.md)

# Como usar:

```
use L2JFacility\L2JFacility;
```
## Ranks
```
L2JFacility::rank('pvpkills', 50); // Primeiro parâmetro Lista os pvps,
segundo parâmetro quantidade de Jogadores por página 
L2JFacility::rank('pvpkills'); // Padrão 10 por página.

Parâmetros suportado pkkills, karma, fame, level, exp, sp, onlinetime
```

## Contadores
```
L2JFacility::count('accounts'); // Parâmetro esperado nome da tabela
L2JFacility::count('characters'); // Parâmetro esperado nome da tabela, 
Parâmetros suportado qualquer nome de tabela da sua database

L2JFacility::online(); // Retorna quantos jogadores estão online.


```

## Boss estado
```
L2JFacility::grandboss(); // Retorna os grandboss e seus nomes e características
L2JFacility::boss(); // Retorna os boss e seus nomes e características. 
Aceita um parâmetro opcional de páginação o padrão é 10 por página
L2JFacility::boss(50); // retorna os 50 primeiro raidboss
```

## Castle e Fortress
```
L2JFacility::castle('d/m/Y - H:i:s'); Parâmetro esperado formato da data 
ele vai retornar todas as informações referente aos castelos.
[Mais formatos](https://www.php.net/manual/pt_BR/function.date.php)
L2JFacility::showCastle('Aden', 'd M Y'); Parâmetro esperado nome do castelo
Aden, Dion, Giran, Gludio, Goddard, Innadril, Oren, Rune, Schuttgart 
e o segundo parâmetro é o formato da data.
Usando o nome do castelo vai retonar informações apenas daquele castelo. 

L2JFacility::fort('d/m/Y - H:i:s'); Parâmetro esperado formato da data 
ele vai retornar todas as informações referente aos fortress.
[Mais formatos](https://www.php.net/manual/pt_BR/function.date.php)
L2JFacility::showFort('Aaru', 'd M Y'); Parâmetro esperado nome do fortress
Aaru, Antharas, Archaic, Bayou, Borderland, Cloud Mountain, Demon, Dragonspine,
Floran,Hive, Hunters, Ivory, Monastic, Narsell, Shanty (...) 
e o segundo parâmetro é o formato da data.
Usando o nome do castelo vai retonar informações apenas daquele castelo. 
```


