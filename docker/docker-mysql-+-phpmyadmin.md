# Docker mysql + phpmyadmin

### Run MySQL

```bash
 $ docker run --name mysql -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mysql:latest
```

### Run phpMyAdmin

```bash
$ docker run --name phpmyadmin -d --link mysql -e PMA_HOST="mysql" -p 8080:80 phpmyadmin
```

Open your browser and go to localhost:8080, then enter account: root and password: root.
