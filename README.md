### Up and running

```
$ docker compose up -d
```

#### To enable rabbitmq prometheus plugin

```
docker exec -it rabbitmq rabbitmq-plugins enable rabbitmq_prometheus
```

#### Add admin user

```
docker exec -it rabbitmq rabbitmqctl add_user admin password
docker exec -it rabbitmq rabbitmqctl set_user_tags admin administrator
docker exec -it rabbitmq rabbitmqctl set_permissions -p / admin ".*" ".*" ".*"
```

#### Check about rabbitmq_prometheus installed

```
docker exec -it rabbitmq rabbitmq-plugins list | grep prometheus
```

#### List queues

```
docker exec -it rabbitmq rabbitmqctl list_queues
```
