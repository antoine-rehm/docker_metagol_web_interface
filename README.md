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
 ```
 docker-compose.exe up -d
 docker cp .\sources\initDB.sql  metagolwebinterface_db_1:/
 docker exec -it  metagolwebinterface_web_1 sh
    mysql -u metagol -pmetagol metagolDB < initDB.sql
```