# Как делать задачи

Вам будут даны задания по написанию модулей:
- `comments` - все что относится к комментариям;
- `orders` - все что относится к заказам;
- `options` - все что относится к дополнительным услугам;
- `prices` - все что относится к тарифам и цене;

Все они пишутся по одной схеме:

1. Создаем папку с названием модуля и создаем в ней пустой `__init__.py`
2. В файле `~/src/client_app/settings.py` вставить название модуля в массив `INSTALLED_APPS = [...]`
3. Создаем файл `modules.py` и папку `migrations/`
4. В `modules.py` описываем таблицу из макета базы данных (можно посмотреть пример в модуле cars)
5. Если в модели встречается тип enum - то нужно описать это в отдельной папке `enums/` ( -//- )
6. После создания необходимо создать миграцию: `python ./src/manage.py makemigrations`

Если выполнить эти шаги, то в базе данных появится таблица в БД.

// Продолжение следует...