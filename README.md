# Commands-and-others
Repository to remembers commands and other problematic things

Removing mysql completely and then reinstall it (* remember that this can be problematic to dbs within the mysql): 
sudo systemctl stop mysql;
sudo apt-get remove mysql-client-8.0 mysql-client-core-8.0 mysql-common mysql-server mysql-server-8.0 mysql-server-core-8.0; # using * wildcard didn't work
sudo apt-get purge mysql-client-8.0 mysql-client-core-8.0 mysql-common mysql-server mysql-server-8.0 mysql-server-core-8.0;
sudo rm -rf /etc/mysql /var/lib/mysql /var/log/mysql;
sudo apt-get autoremove;
sudo apt-get autoclean;
sudo apt update;
sudo apt install mysql-server;
