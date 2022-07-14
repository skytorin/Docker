# Docker 


## Установка Docker
### Ручая установка
```bash
curl -L get.docker.com | bash
```

### Установка через APT
1. Обновление базы пакетов:
```bash
sudo apt update
```

2. Позволяем APT использовать пакеты через HTTPS:
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

3. Добавление ключа GPG для официального репозитория Docker:
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

4. Добавление репозитория Docker в источники APT:
```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```

5. Обновление базы пакетов:
```bash
sudo apt update
```

6. Необязательный шаг для проверки источника установки;
```bash
apt-cache policy docker-ce
```

7. Установка Docker:
```bash
sudo apt install docker-ce
```

### Общие послеустановочные шаги
Добавление пользователя в группу docker (чтобы не использовать sudo):
```bash
sudo usermod -aG docker ${USER}
```

Проверка, успешного добавления пользователя в группу Docker:
```bash
id -nG
```
Проверка статуса:
```bash
sudo systemctl status docker
 или
sudo service docker status
```

Запуск службы Docker:
```bash
sudo systemctl start docker
 или
sudo service docker start
```

Проверка версии Docker:
```bash
docker --version
```


## Команды Docker
### Работа с images 
Просмотр имеджей в локальном репозитарии:
```bash
docker images
```

Удаление имеджа из локального репозитария: 
```bash
docker rmi nginx
docker rmi {id}
docker rmi -f {id}
```

Удаление неиспользуемых (dangling) образов
```bash
docker image prune
docker rmi $(docker images -f dangling=true -q)
```

Удаление неиспользуемых (dangling) образов даже с тегами
```bash
docker image prune -a
```

Удаление всех образов
```bash
docker rmi $(docker images -a -q)
```

Удаление всех образов без тегов
```bash
docker rmi -f $(docker images | grep "^<none>" | awk "{print $3}")
```

Создание образов
```bash
docker build .
docker build github.com/creack/docker-firefox
docker build - < Dockerfile
docker build - < context.tar.gz
docker build -t eon/infinite .
docker build -f myOtherDockerfile .
curl example.com/remote/Dockerfile | docker build -f - .
```

Загрузка репозитория в tar (из файла или стандартного ввода)
```bash
docker load < ubuntu.tar.gz
docker load --input ubuntu.tar
```

Сохранение образа в tar-архив
```bash
docker save busybox > ubuntu.tar
```

Создание образа из контейнера
```bash
docker commit nginx
```

Тегирование образа
```bash
docker tag nginx eon01/nginx
```

### Работа с контейнерами
Первый запуск контейнера
```bash
docker run -it --name infinite -d eon01/infinite
```

Запуск контейнера из образа с переходом в шелл контейнера:
```bash
docker run -it skytorin:alpine
```

Запуск контейнера из образа + в фоне + создание имени для контейнера + мапинг локального порта 8080 на порт 80 контейнера:
```bash
docker run --name skytorin_nginx -d -p 8080:80 skytorin:nginx
```

Доступ к консоли контейнера:
```bash
docker exec -it skytorin/alpine:latest /bin/sh
```

Создание контейнера
```bash
docker create -t -i eon01/infinite --name infinite
```

Запуск контейнера
```bash
docker start nginx
```

Перезагрузка контейнера
```bash
docker restart nginx
```

Пауза (приостановка всех процессов контейнера)
```bash
docker pause nginx
```

Продолжение работы контейнера после паузы
```bash
docker unpause nginx
```

Блокировка (до остановки контейнера)
```
docker wait nginx
```

Остановка контейнера
```bash
docker stop nginx
```

Отправка SIGKILL (завершающего сигнала)
```bash
docker kill nginx
```

Отправка другого сигнала
```bash
docker kill -s HUP nginx
```

Подключение к существующему контейнеру
```bash
docker attach nginx
```

Удаление работающего контейнера
```bash
docker rm nginx
```

Удаление контейнера и его тома (volume)
```bash
docker rm -v nginx
```

Удаление всех контейнеров со статусом exited
```bash
docker rm $(docker ps -a -f status=exited -q)
```

Удаление всех остановленных контейнеров
```bash
docker container prune
docker rm `docker ps -a -q`
```

Удаление контейнеров, остановленных более суток назад
```bash
docker container prune --filter "until=24h"
```

Остановка и удаление всех контейнеров
```bash
docker stop $(docker ps -a -q) && docker rm $(docker ps -a -q)
```

Переименование контейнера
```bash
docker rename infinite infinity
```

Обновление контейнера
```bash
docker update --cpu-shares 512 -m 300M infinite
```

### Работа с удаленным репозитарием образов
Вход в реестр
```bash
docker login --username skytorin
docker login localhost:8080
```

Выход из реестра
```bash
docker logout
docker logout localhost:8080
```

Поиск образа
```bash
docker search nginx
docker search nginx -- filter stars=3 --no-trunc busybox
```

Pull (выгрузка из реестра) образа
```bash
docker pull nginx
docker pull skytorin/alpine:latest 
docker pull eon01/nginx localhost:5000/myadmin/nginx
```

Push (загрузка в реестр) образа
```bash
docker push new-repo:tagname
docker push skytorin/alpine:latest 
docker push eon01/nginx
docker push eon01/nginx localhost:5000/myadmin/nginx
```


```bash
docker tag local-image:tagname new-repo:tagname
```

### Диагностика работы контейнера
Вывод информации о запущенных контейнерах
```bash
docker ps
```

Вывод информации о всех имеющихся контейнерах
```bash
docker ps -a
```

Интерактивная информация о использовании ресурсов хоста запущенными контейнерами
```bash
docker stats
```

Вывод логов контейнера
```bash
docker logs nginx
```

События контейнера
```bash
docker events infinite
```

Публичные порты
```bash
docker port infinite
```

Выполняющиеся процессы
```bash
docker top infinite
```

Информация о контейнере
```bash
docker inspect nginx
docker inspect --format '{{ .NetworkSettings.IPAddress }}' $(docker ps -q)
```

Просмотр истории образа
```bash
docker history nginx:alpine
```

### Работа с volumes
Список томов:
```bash
docker volume ls
```

Каталог расположения volumes по умолчанию
```bash
ls /var/lib/docker/volumes/
```

Удаление неиспользуемых (dangling) томов
```bash
docker volume prune
docker volume rm $(docker volume ls -f dangling=true -q)
```

Удаление неиспользуемых (dangling) томов по фильтру
```bash
docker volume prune --filter "label!=keep"
```

### Работа с сетью
Создание сети
```bash
docker network create -d overlay MyOverlayNetwork
docker network create -d bridge MyBridgeNetwork
docker network create -d overlay \
  --subnet=192.168.0.0/16 \
  --subnet=192.170.0.0/16 \
  --gateway=192.168.0.100 \
  --gateway=192.170.0.100 \
  --ip-range=192.168.1.0/24 \
  --aux-address="my-router=192.168.1.5" --aux-address="my-switch=192.168.1.6" \
  --aux-address="my-printer=192.170.1.5" --aux-address="my-nas=192.170.1.6" \
  MyOverlayNetwork
```

Удаление сети
```bash
docker network rm MyOverlayNetwork
```

Список сетей
```bash
docker network ls
```

Получение информации о сети
```bash
docker network inspect MyOverlayNetwork
```

Подключение работающего контейнера к сети
```bash
docker network connect MyOverlayNetwork nginx
```

Подключение контейнера к сети при его запуске
```bash
docker run -it -d --network=MyOverlayNetwork nginx
```

Отключение контейнера от сети
```bash
docker network disconnect MyOverlayNetwork nginx
```

Удаление неиспользуемых сетей
```bash
docker network prune
```

### Разное
Удаление всех неиспользуемых объектов
```bash
docker system prune
```

По умолчанию для Docker 17.06.1+ тома не удаляются. Чтобы удалились и они тоже:
```bash
docker system prune --volumes
```

Создание образа из dockerfile
```bash
docker build
```

Изменения в файлах или директориях файловой системы контейнера
```bash
docker diff infinite
```
