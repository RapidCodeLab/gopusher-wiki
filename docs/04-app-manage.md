## Application Managment

After successfully installing the application, there are three simple commands you will use to manage your application:

### Run
```bash
docker-compose up -d
```
### Stop
```bash
docker-compose stop
```
### Update
```bash
docker-compose pull
```

### Show logs
```bash
docker-compose logs {container_name}
```
The container names will be webapp, senderapp, eventsapp, etc.