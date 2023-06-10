## Экзамен по КПО второй курс
####  Хамид Карим БПИ214

Для установки необходим лишь docker. 

Для запуска необходимо лишь поднять docker-compose:
```bash
docker-compose up --build
```

При запуске, бд будет пустая. Если хочется протестировать на данных, можно войти в контейнер django и создать суперпользователя.
```bash
docker ps
docker exec -it <id контейнера django> bash

$ python3 manage.py createsuperuser  
```
Далее можно входить по localhost:8000/admin и в удобном формате добавить песни.

Все API реализованы по заданию. Данные на сервер (в POST запросах) отправляются в виде JSON. 

При создании плейлиста требуется использовать следующий формат:
```json
{
    "name": "Любимые"
}
```

При добавлении песни формат:
```json
{
    "song_id": 4
}
```