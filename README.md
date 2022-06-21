# DUMMYAPI.IO
## Оглавление

[Описание проекта DUMMYAPI.IO](#Описание-проекта-DUMMYAPI.IO)   

   - [POST](#POST)
       - [GET /post (Get List)](#GET-/-post-(Get-List))
       - [GET /user/:id/post (Get List By User)](#GET-/-user-/-:id-/-post-(Get-List-By-User))
       - [GET/tag/:id/post (Get List By Tag)](#GET-/-tag-/-:id-/-post- (Get-List-By-Tag))     
## Описание проекта DUMMYAPI.IO
https://dummyapi.io/ представляет собой сервис для тестирования АПИ. Для выполнения запросов необходим app-id, который генерируется автоматически при регистрации на сервисе. В качестве тестирования были взяты следующие объекты:
### POST 
____
**GET /post (Get List)**

Возвращает список публикаций отсортировнных по дате.
 - доступен query params для вывода определенной страницы.
 - доступен query params для отображения числа публикаций на странице.
 
**Response Body:**

 **List**
 ```js
 {
data: Array(Model)
total: number(total items in DB)
page: number(current page)
limit: number(number of items on page)
}
```
**Post Preview**
```js
{
id: string(autogenerated)
text: string(length: 6-50, preview only)
image: string(url)
likes: number(init value: 0)
tags: array(string)
publishDate: string(autogenerated)
owner: object(User Preview)
}
```
**GET /user/:id/post (Get List By User)**

Получить список записей для конкретного пользователя, отсортированных по дате создания.
- Доступны параметры запроса разбивки на страницы.
- Доступны созданные параметры запроса.

**Response Body:**

 **List**
 ```js
 {
data: Array(Model)
total: number(total items in DB)
page: number(current page)
limit: number(number of items on page)
}
```
**Post Preview**
```js
{
id: string(autogenerated)
text: string(length: 6-50, preview only)
image: string(url)
likes: number(init value: 0)
tags: array(string)
publishDate: string(autogenerated)
owner: object(User Preview)
}
```
**GET/tag/:id/post (Get List By Tag)**

Получите список записей для определенного тега, отсортированных по дате создания.
- Доступны параметры запроса разбивки на страницы.
- Доступны созданные параметры запроса.

**Response Body:**

 **List**
 ```js
 {
data: Array(Model)
total: number(total items in DB)
page: number(current page)
limit: number(number of items on page)
}
```
**Post Preview**
```js
{
id: string(autogenerated)
text: string(length: 6-50, preview only)
image: string(url)
likes: number(init value: 0)
tags: array(string)
publishDate: string(autogenerated)
owner: object(User Preview)
}
```
