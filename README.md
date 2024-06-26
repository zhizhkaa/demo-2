# Примеры использования API
## Получение списка всех объектов
```sh
curl -X GET http://localhost:8080/items
```
### Ожидаемый ответ:
```json
[
  {
    "id": 1,
    "name": "Sample Item",
    "quantity": 10
  },
  {
    "id": 2,
    "name": "Another Item",
    "quantity": 5
  }
]
```
## Получение объекта по ID
```sh
curl -X GET http://localhost:8080/items/1
```
### Ожидаемый ответ:
```json
{
  "id": 1,
  "name": "Sample Item",
  "quantity": 10
}
```
## Создание нового объекта
```sh
curl -X POST http://localhost:8080/items \
-H "Content-Type: application/json" \
-d '{
  "name": "Sample Item",
  "quantity": 10
}'
```
### Ожидаемый ответ:

```json
{
  "id": 3,
  "name": "Sample Item",
  "quantity": 10
}
```
## Обновление существующего объекта
```sh
curl -X PUT http://localhost:8080/items/1 \
-H "Content-Type: application/json" \
-d '{
  "name": "Updated Item",
  "quantity": 20
}'
```
### Ожидаемый ответ:
```json
{
  "id": 1,
  "name": "Updated Item",
  "quantity": 20
}
```
## Удаление объекта
```sh
curl -X DELETE http://localhost:8080/items/1
```
