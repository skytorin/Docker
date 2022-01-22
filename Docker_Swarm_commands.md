# Docker Swarm
## Установка Swarm
Установка Docker Swarm
```bash
curl -ssl https://get.docker.com | bash
```

## Команды Swarm
Инициализация Swarm
```bash
docker swarm init --advertise-addr 192.168.10.1
```

Подключение рабочего узла (worker) к Swarm
```bash
docker swarm join-token worker
```

Подключение управляющего узла (manager) к Swarm
```bash
docker swarm join-token manager
```

Список сервисов
```bash
docker service ls
```

Список узлов
```bash
docker node ls
```

Создание сервиса
```bash
docker service create --name vote -p 8080:80 instavote/vote
```

Список заданий Swarm
```bash
docker service ps
```

Масштабирование сервиса
```bash
docker service scale vote=3
```

Обновление сервиса
```bash
docker service update --image instavote/vote:movies vote
docker service update --force --update-parallelism 1 --update-delay 30s nginx
docker service update --update-parallelism 5--update-delay 2s --image instavote/vote:indent vote
docker service update --limit-cpu 2 nginx
docker service update --replicas=5 nginx
```






