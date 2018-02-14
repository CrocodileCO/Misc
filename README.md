Для резервного копирования используеться mongodump, которая по умолчанию идет в пакете с сервером.
Создание бекапа всей БД :

mongodump -h localhost -d DATABASE_NAME -o BACKUP_FOLDER

Также можно делать бекап определённых коллекций:

mongodump --db blog --collection posts

На выходе мы получаем папку с файлами в формате BSON.
Для восстановление бекапа:

mongorestore -h localhost -d DATABASE_NAME BACKUP_FOLDER
