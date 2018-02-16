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

