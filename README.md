# golang hexagonal architecture

1. For install the dependencies: 

```
go mod tidy
```

2. For create table in database

```
docker compose exec mysql bash
mysql -uroot -p products
root

create table products (id varchar(255), name varchar(255), price float);
```

3. For create topic in Kafka:

```
docker compose exec kafka bash
kafka-topics --bootstrap-server=localhost:9092 --topic=products --create
```
4. For run application

```
docker compose exec goapp bash
go run cmd/app/main.go

```

5. For test API Rest, you can use the requests that be in test.http file

6. For test the kafka

```
docker compose exec kafka bash
kafka-console-producer --bootstrap-server=localhost:9092 --topic=products
{"name": "My Product2", "price": 200}
```
