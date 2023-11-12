# Tutorial2: Nginx + Flask + MySQL

## DB server (EC2 instance in Private subnet)

```
docker-compose -f compose.yaml.db up -d
```

## Web server + backend (EC2 instance in Public subnet)