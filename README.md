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
