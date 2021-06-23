# MYSQL Commands;

## 1- Removing and installing/reinstalling:
Removing mysql completely and then reinstall it (* remember that this can be problematic to dbs within the mysql, and will remove workbench):

```
sudo systemctl stop mysql;
sudo apt-get remove mysql-client-8.0 mysql-client-core-8.0 mysql-common mysql-server mysql-server-8.0 mysql-server-core-8.0; # using * wildcard didn't work
sudo apt-get purge mysql-client-8.0 mysql-client-core-8.0 mysql-common mysql-server mysql-server-8.0 mysql-server-core-8.0;
sudo rm -rf /etc/mysql /var/lib/mysql /var/log/mysql;
sudo apt-get autoremove;
sudo apt-get autoclean;
sudo apt update;
sudo apt install mysql-server;
```

## 2- Creating a new connection:

``` 
(sudo) mysql -u root -p; # enter into mysql through bash terminal;

mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'your_password'; flush privileges; 
# the quotes are necessary, as it only accepts strings;
# if everything went OK, it will show.
mysql> exit # to leave
```
