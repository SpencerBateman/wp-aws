# How to install Wordpress on ec2

### Install Apache
`sudo yum install httpd`

`sudo service httpd start`

now check to see if your server is running by checking the url `http://ec2-50-17-15-27.compute-1.amazonaws.com`

### Install PHP

`sudo yum install php php-mysql`

restart apache

`sudo service httpd restart`


test the php installation by creating a dummy page.

create `test.php` in the directory `/var/www/html`

in `test.php` have write one line `<?php phpinfo() ?>`

test to see if it is working by visting `http://ec2-50-17-15-27.compute-1.amazonaws.com/test.php`

### Install mysql

`sudo yum install mysql-server`

start mysql

`sudo service mysqld start`

Create a database named wordpress

`mysqladmin -u root create blog`

Secure the database

`sudo mysql_secure_installation`

Answer the questions as follows 

* Enter current password for root: Press return for none
* Change Root Password: Y
* New Password: Enter your new password
* Remove anonymous user: Y
* Disallow root login remotely: Y
* Remove test database and access to it: Y
* Reload privilege tables now: Y

### Install Wordpress
