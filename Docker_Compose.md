# Docker Compose
## Установка Docker Compose
Проверяем последнюю версию релиза на странице https://github.com/docker/compose/releases
Загружаем версию 1.29.2 и сохраняет исполняемый файл в каталоге /usr/local/bin/docker-compose
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo curl -L "https://github.com/docker/compose/releases/download/v2.2.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Задаём правильные разрешения, чтобы сделать команду docker-compose исполняемой
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

Проверяем успешность установки
```bash
docker-compose --version 
```

## Настройка файла docker-compose.yml
Cоздаём новый каталог в домашнем каталоге и перейдите в него
```bash
mkdir ~/compose-demo
cd ~/compose-demo
```

Настройте в этом каталоге папку приложения, которая будет выступать в качестве корневого каталога документов для вашей среды Nginx
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

Просмотр информации о запущенном контейнера
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

Остановка выполнения контейнеров, не уничтожает данные, связанные контейнерами
```bash
docker-compose stop
```

Удаление контейнеров, сетей и томов, связанных с контейнерной средой
```bash
docker-compose down
```

