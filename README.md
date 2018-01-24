 # Metagol Docker Web Interface
This is the web interface for metagol (https://github.com/metagol/metagol) dockerise.
# sources/constants.php config values to replace
$constant['mysqlServer'] = "db";
$constant['mysqlUser'] = "metagol";
$constant['mysqlPassword'] = "metagol";
$constant['mysqlDB'] = "metagolDB";

$execStr = "yap";

$dirName = "//srv//metagol//temp";
 
# How to run
- Up docker:
```
docker-compose up -d
````
- Copy sql init script to mariadb docker
  linux:
  ```
  docker cp ./sources/initDB.sql  dockermetagolwebinterface_db_1:/
  ```
  windows:
  ```
  docker cp .\sources\initDB.sql  dockermetagolwebinterface_db_1:/
  ```
- Execute sh and execute sql initi script
```
docker exec -it  dockermetagolwebinterface_web_1 sh
    mysql -u metagol -pmetagol metagolDB < initDB.sql
```