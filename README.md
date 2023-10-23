# Домашняя работа №12.2 "Работа с данными (DDL/DML)" - Одинцов Игорь

### Задание 1

1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp.

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

1.4. Дайте все права для пользователя sys_temp.

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

1.6. Переподключитесь к базе данных от имени sys_temp.
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

1.7. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.8. Восстановите дамп в базу данных.

1.9. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

### Ответ

Создание учетной записи командой:
create user 'sys_temp'@'localhost' IDENTIFIED BY 'pass';

Выполните запрос на получение списка пользователей в базе данных:
![user](https://github.com/Bestenar/12.2-DDL_DML-hw/assets/111271419/54bd0600-fbe3-4f9e-8fd0-c60fe8e843a1)

Выдаем права созданному пользователю:
GRANT ALL PRIVILEGES ON * . * TO 'sys_temp'@'localhost' WITH GRANT OPTION; FLUSH PRIVILEGES;

Выполните запрос на получение списка прав для пользователя sys_temp:
![grant](https://github.com/Bestenar/12.2-DDL_DML-hw/assets/111271419/4b9343e7-05f4-4e45-93f7-587fd8645b45)

Переподключитесь к базе данных от имени sys_temp:
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных и восстанавливаем его в базу данных.

![diagram](https://github.com/Bestenar/12.2-DDL_DML-hw/assets/111271419/6a12db3f-938b-4948-9841-8646b671a1a6)


### Задание 2

Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц.

### Ответ

| Название таблицы  | Название первичного ключа |
| ------------- | ------------- |
| language  | language_id  |
| film  | film_id  |
| category  | category_id  |
| film_category  | film_id; category_id  |
| actor | actor_id  |
| film_actor  | actor_id; film_id  |
| film_text  | film_id  |
| inventory  | inventory_id  |
| customer  | customer_id  |
| rental  | rental_id  |
| payment  | payment_id  |
| store  | store_id  |
| staff  | staff_id  |
| address  | adress_id  |
| city  | city_id  |
| country  | country_id  |
