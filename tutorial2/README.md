# Tutorial2: Nginx + Flask + MySQL

## DB server (EC2 instance in Private subnet)

```
docker-compose -f compose.yaml.db up -d
```

Test

```
curl -v telnet://localhost:3306
```

Connect DB server from EC2 instance in Public subnet with mysql client.

```
mysql -u root -p test_db -P 3306 --protocol tcp --host=10.0.2.146
```

* private ip address of EC2 instance in private subnet: 10.0.2.146

## Web server + backend (EC2 instance in Public subnet)

```
docker-compose up -d
```