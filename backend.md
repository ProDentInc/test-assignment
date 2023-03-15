# Тестовое задание для Backend-разработчика

## Задание

Создать Laravel приложение с использованием пакета Lighthouse PHP для GraphQL.

### Дано:

* Модель ```Specialization``` с полями ```id```, ```name```, ```parent_id (nullable)```
  * Специализация может [ссылаться]((https://lighthouse-php.com/5/api-reference/directives.html#belongsto)) на другую специализацию (родительская специализация);
* Модель ```UserStatus``` с полями ```id```, ```name```, ```code```;
* Модель ```User```
  * Пользователь [имеет статус](https://lighthouse-php.com/5/api-reference/directives.html#belongsto);
  * Пользователь может [иметь несколько специализаций](https://lighthouse-php.com/5/api-reference/directives.html#hasmanythrough).

### Задача

* Создать GraphQL [схему для моделей](https://lighthouse-php.com/5/the-basics/types.html#object-type) ```Specialization```, ```UserStatus```, ```User```;
* Создать GraphQL запросы для получения данных о специализациях, статусах пользователей и пользователях
  * Для пользователей сделать 3 запроса: 
    * Получение пользователей с [пагинацией](https://lighthouse-php.com/5/api-reference/directives.html#paginate);
    * Получение [всех пользователей списком](https://lighthouse-php.com/5/api-reference/directives.html#all);
    * Получение пользователя [по ID](https://lighthouse-php.com/5/api-reference/directives.html#find).
* [Создать GraphQL мутацию](https://lighthouse-php.com/master/the-basics/fields.html#fields-with-arguments) для создания пользователя вместе с новой специализацией.

### Необязательное

* Сидирование данных для всех моделей.

### Требуемый стек технологий
* PHP 8.1+;
* Laravel 9+; 
* Lighthouse PHP; 
* MySQL.

### Технологии по желанию

* Docker.

### Требования к качеству приложения и коду

* Чистый и читабельный код; 
* Валидация входных данных.

## Полезные ссылки:
* Документация [Lighthouse PHP](https://lighthouse-php.com/);
* [Плагин GraphQL для Jetbrains IDE](https://plugins.jetbrains.com/plugin/8097-graphql);
* Пакет [laravel-graphiql](https://github.com/mll-lab/laravel-graphiql) для тестирования GraphQL запросов.
