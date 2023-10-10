## Linux - Connect DataBase
---
### MySQL
```
sudo dnf update -y
sudo dnf install -y mariadb105
mysql -h <RDS MySQL Writer Endpoint> -P <Port> -u <User Name> -p
```

<br>

### PostgreSQL
```
sudo dnf update -y
sudo dnf install -y postgresql15
psql --host=<RDS PostgreSQL Writer Endpoint> --port=<Port> --username=<User Name> --password --dbname=<DataBase Name>
```