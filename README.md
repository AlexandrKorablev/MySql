# MySql
Работа с БД
___

_Создание стола._
```mysql
CREATE TABLE dns_users_samara (

id int,
fname varchar(50),
lname varchar(50),
age int,
num_phone int
);
```
![Создание стола](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(5).png)
___
_Заполнение колонн._
```mysql
use dnsshop;
INSERT INTO phones (`brand`, `memory`, `color`, `price`) VALUES ('apple', '32gb', 'white', '36000');
INSERT INTO phones (`brand`, `memory`, `color`, `price`) VALUES ('samsung', '642gb', 'black', '13500');
INSERT INTO phones (`brand`, `memory`, `color`, `price`) VALUES ('xiaomi', '64gb', 'gray', '9000');
INSERT INTO phones (`brand`, `memory`, `color`, `price`) VALUES ('oppo', '128gb', 'blue', '7000');
INSERT INTO phones (`brand`, `memory`, `color`, `price`) VALUES ('pixel', '62gb', 'black', '60000');
```
![Создание стола](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(2).png)
___
_Изменение в поле колонны._
```mysql
use dnsshop;
UPDATE `phones`
SET `memory` = '64gb'
WHERE `id` = 2;
```
![Создание стола](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(3).png)
___
_Изменения в колоннах._
```mysql
use dnsshop;
ALTER TABLE `phones`
VARCHAR(45) NULL AFTER `brand`;
```
![Создание стола](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(4).png)
___
_Удаление стола._
```mysql
DROP TABLE `dns_users1`;
```
![Создание стола](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(1).png)
___
_Поиск значения > чем..._
```mysql
use dnsshop;
SELECT * FROM phones WHERE id > 3;
```
![Поиск](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(6).png)
___
_Поиск лимит_
```mysql
use dnsshop;
SELECT * FROM phones LIMIT 4;
```
![Поиск](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(7).png)
___
_Поиск по ID_
```mysql
use dnsshop;
SELECT * FROM phones WHERE id = 4;
```
![Поиск](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(8).png)
___
_Поиск по бренду и цене < указанной_
```mysql
use dnsshop;
SELECT * FROM phones WHERE (brand = 'apple') AND (price < 25000);
```
![Поиск](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(9).png)
___
_Поиск по столбцу бренд_
```mysql
use dnsshop;
SELECT * FROM phones WHERE brand = "apple";
```
![Поиск](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(10).png)
___
_Поиск по модели >, лимит_
```mysql
use dnsshop;
SELECT * FROM phones WHERE model > 4 LIMIT 3;
```
![Поиск](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(11).png)
___
_Поиск по столбцу_
```mysql
use dnsshop;
SELECT memory FROM phones;
```
![Поиск](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(12).png)
___
_Сортировка по возрастанию_
```mysql
use dnsshop;
SELECT * FROM phones ORDER BY price;
```
![Поиск](https://github.com/AlexandrKorablev/MySql/blob/main/mySQL%20(13).png)
