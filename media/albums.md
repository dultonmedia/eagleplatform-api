## Получение списка альбомов

    GET https://api.eagleplatform.com/api/v2/albums.json

Пример:

    curl 'https://api.eagleplatform.com/api/v2/albums.json?account=smth&auth_token=***'

Пример результата:

    {
        "data": [{
            "id": 10000,
            "name": "Альбом 1",
            "total_records": 10,
            "children": [{
                "id": 10001,
                "name": "Альбом 2",
                "total_records": 2,
                "children": []
            }]
        },{
            "id": 10002,
            "name": "Альбом 3",
            "total_records": 5,
            "children": []
        }]
    }


## Создание альбома

    POST http://api.eagleplatform.com/api/v2/albums.json

Параметры:

* `name` - название

* `parent_id` - идентификатор родительской записи (для вложенных альбомов)

Пример:

    curl -d "{"name":"album_name"}" -X POST 'https://api.eagleplatform.com/api/v2/albums.json?account=smth&auth_token=***'

## Редактирование альбома

    PATCH http://api.eagleplatform.com/api/v2/albums/{id}.json

Параметры:

* `id` - идентификатор

* `name` - название

* `parent_id` - идентификатор родительской записи (для вложенных альбомов)

Пример:

    curl -d "{"name":"updated_album_name"}" -X PATCH 'https://api.eagleplatform.com/api/v2/albums/10000.json?account=smth&auth_token=***'

## Удаление альбома

    DELETE http://api.eagleplatform.com/api/v2/albums/{id}.json

## Получение списка записей в альбоме

    GET https://api.eagleplatform.com/api/v2/albums/{id}/records.json

Пример:

    curl 'https://api.eagleplatform.com/api/v2/albums/{10000}/records.json?account=smth&auth_token=***'

Пример результата:

    {
        "data": [{
            "id": 100500,
            "name": "Record name",
            "description": "Record description",
            "duration": 20000,
            ...

