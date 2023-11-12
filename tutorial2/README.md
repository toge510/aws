# Tutorial2: Nginx + Flask + MySQL

## DB server (EC2 instance in Private subnet)

```
docker-compose -f compose.yaml.db up -d
```

Test

```
curl -v telnet://localhost:3306
```

* private ip address of EC2 instance in private subnet: 10.0.2.146

## Web server + backend (EC2 instance in Public subnet)

```
docker-compose up -d
```

Check

```
curl localhost
```

Access public ip address.

```
Hello Blog post #1
Hello Blog post #2
Hello Blog post #3
Hello Blog post #4
```