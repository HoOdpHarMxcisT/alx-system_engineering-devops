# Mysql :page_with_curl: 0x14-mysql

## About this project :bulb:

In this project, I learned how to set up database backups on web servers using
using `MySQL` in a `Ubuntu` server. I configured the primary-replica setup(Master-Slave replication) on two servers.
This is an outline of the steps I took to configure a MySQL instance on one server as a source database and then configure a 
MySQL instance on another server to function as its replica. It also includes an overview of how MySQL handles replication.

* Install Mysql on both servers:
    - copy signature key for package verification at https://dev.mysql.com/doc/refman/5.7/en/checking-gpg-signature.html
    key is present in file 'signature.key'. Save key in a file 'signature.key' on server
    - add the key to the server's apt keyring:
    sudo apt-key add signature.key
    - add the apt repo to the server's sources list:
    sudo sh -c 'echo "deb http://repo.mysql.com/apt/ubuntu bionic mysql-5.7" >> /etc/apt/sources.list.d/mysql.list'
    - update the package list:
    sudo apt-get update
    - Install the mysql server 5.7:
    sudo apt install -f mysql-client=5.7* mysql-community-server=5.7* mysql-server=5.7*

