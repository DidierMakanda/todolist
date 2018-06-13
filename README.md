
Installation and use

```bash
cd /var/www/ or cd yourlocalhostfolder
$ git clone https://github.com/DidierMakanda/todolist.git
$ cd todolist
$ curl -s https://getcomposer.org/installer | php
```
Configure db:

create empty database: i.e. "angularphp"

set config in bootstrap.php
```php
define("DBHOST", '127.0.0.1');
define("DBDRIVER", 'pdo_mysql');
define("DBNAME", 'angularphp');
define("DBUSER", 'root');
define("DBPASS", '1');
define("DEBUG", 1);
```
then run
```bash
$ php composer.phar install
$ php vendor/bin/doctrine orm:schema-tool:update --force
```
Open app in browser in [http://localhost/todolist]


If cache giving you error, add the following in composer.json: ["doctrine/cache": "~1.6.2"]

