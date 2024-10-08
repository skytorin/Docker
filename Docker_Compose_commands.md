# Docker Compose


## Установка Docker Compose
1. Проверяем последнюю версию релиза на странице https://github.com/docker/compose/releases  
Загружаем необходимую версию 1.х.х или 2.х.х и сохраняем исполняемый файл в каталоге /usr/local/bin/docker-compose:
```bash
export DOCKER_COMPOSE_VERSION=v2.3.4
sudo curl -L "https://github.com/docker/compose/releases/download/${DOCKER_COMPOSE_VERSION}/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

2. Задаём правильные разрешения, чтобы сделать команду docker-compose исполняемой:
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

3. Проверяем версию docker-compose:
```bash
docker-compose --version 
```

## Настройка файла docker-compose.yml
Cоздаём новый каталог в домашнем каталоге и переходим в него
```bash
mkdir ~/compose-demo
cd ~/compose-demo
```

Настраиваем в этом каталоге папку приложения, которая будет выступать в качестве корневого каталога документов среды Nginx
```bash
mkdir my_app
```

Создаём в текстовом редакторе новый файл index.html в папке my_app
```bash
vi my_app/index.html
```

Cоздаём файл docker-compose.yml
```bash
vi my_app/docker-compose.yml
```

## Команды для работы с Docker Compose
Запуск контейнера в фоновом режиме
```bash
docker-compose up -d
```

Просмотр информации о запущенном контейнере
```bash
docker-compose ps
```

Просмотр журналов контейнера
```bash
docker-compose logs
```

Приостановка работы среды без изменения текущего состояния контейнеров
```bash
docker-compose pause
```

Возобновление работы после приостановки
```bash
docker-compose unpause
```

Остановка выполнения контейнеров, не уничтожает данные, связанные с контейнерами
```bash
docker-compose stop
```

Удаление контейнеров, сетей и томов, связанных с контейнерной средой
```bash
docker-compose down
```

