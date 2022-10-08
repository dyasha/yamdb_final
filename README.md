![build](https://github.com/dyasha/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

# CI и CD проекта api_yamdb


## Инструкция по запуску 

- Клонируйте проект в свой репозиторий:
```git clone...```
- Или просто перейдите по адресу:
```158.160.5.146/api/v1/ ```

## Примеры
Зарегистривать пользователя и получить confirmation_code на email:
```
POST http://158.160.5.146/api/v1/auth/signup/
Content-Type: application/json

{
    "username": "user1",
    "email": "user1@me.ru"
} 
```
Получить токен пользователя:
```
POST http://158.160.5.146/api/v1/auth/token/
Content-Type: application/json

{
    "username": "user1",
    "confirmation_code": "7IwAK7A9_HvEivqlkBx-hDkPdrFI96AGPZ4gitGXbRw"
}
```
Получить список зарегистрированных пользователей от имени администратора:
```
GET http://158.160.5.146/api/v1/users/
Authorization: Bearer xxxxxxx

```
Добавить пользователя от имени администратора:
```
POST http://158.160.5.146/api/v1/users/
Authorization: Bearer xxxxx
Content-Type: application/json

{
    "username": "user2",
    "email": "user2@me.ru",
    "role": "user"
}
```
