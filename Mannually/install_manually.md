# Install MariaDB

Install MariaDB
```
sudo apt install software-properties-common
```

If you are on version Ubuntu 20.04, then MariaDB is available in default repo and you can directly run the below commands to install it:
```
sudo apt-get update
sudo apt-get install mariadb-server
```
During this installation you'll be prompted to set the MySQL root password. If you are not prompted, you'll have to initialize the MySQL server setup yourself. You can do that by running the command:

```
mysql_secure_installation
```

# Connection from Remote System

Install mariadb-client
```
apt-get install mariadb-client-10.3
```

and change the following part bind-address of the file /etc/mysql/mariadb.conf.d/50-server.cnf

```
#user                    = mysql
pid-file                = /run/mysqld/mysqld.pid
basedir                 = /usr
#datadir                 = /var/lib/mysql
#tmpdir                  = /tmp

# Broken reverse DNS slows down connections considerably and name resolve is
# safe to skip if there are no "host by domain name" access grants
#skip-name-resolve

# Instead of skip-networking the default is now to listen only on
# localhost which is more compatible and is not less secure.
bind-address            = 0.0.0.0
```
