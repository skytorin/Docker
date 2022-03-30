# Резервное копирование базы данных Wiki.js

## Основные команды PSQL:
Основные команды, которые используются для подключения к БД Postgre, просмотра списка БД
```
$psql -h localhost -p 5416 -U <my-user> -d <my-database>
$psql -p 5432 -U wikijs -d wiki
wiki=# \l  # показать базы данных
wiki=# \q  # выход
```

## Процедура резервного копирования
1. Остановите клиент БД (в нашем случае это контейнер c приложением wiki.js)
```
docker stop app_wikijs_wiki_1 
```
2. Создаем резервную копию БД в volume контейнера или произвольном месте:
```
docker exec app_wikijs_db_1 pg_dumpall -U wikijs > /var/lib/postgresql/backup_wiki.sql
```
или
```
docker exec app_wikijs_db_1 pg_dumpall -U wikijs > backup_wiki_`date +%d-%m-%Y"_"%H_%M_%S`.sql
```

## Процедура восстановления
1. Останавливаем клиента БД (в нашем случае это контейнер с приложением wiki.js)
```
docker stop app_wikijs_wiki_1 
```
2. Удаляем текущую базу данных:
```
docker exec -it app_wikijs_db_1 dropdb -U wikijs wiki
```
3. Создаем новую базу данных:
```
docker exec -it app_wikijs_db_1 createdb -U wikijs wiki
```
4. Восстанавливаем базу данных из бэкапа:
```
cat backup.wiki.sql | docker exec -i app_wikijs_db_1 psql -U wikijs wiki
```
5. Запускаем контейнер c приложением wiki.js
```
docker start app_wikijs_wiki_1  
```

## Дополнительные команды
Копирование контейнера в локальную систему:
```
docker cp -a [container_name]:/wiki C:\Users\jcr\Desktop\docker_yml\backup_db
```
Подключаемся к контейнеру с postgre:
```
docker exec -it app_wikijs_db_1 psql -p 5432 -U wikijs -d wiki
```
Для передачи файлов между контейнером и хостом можно использовать FTP. 
В качестве сервера FTP исполбьзуем vsftpd с базовой конфигурацией.
Используем systemd для запуска службы
```
systemctl start vsftpd
```
В качестве клиента FTP можно использовать Filezilla.
