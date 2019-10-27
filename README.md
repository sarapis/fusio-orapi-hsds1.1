# miami211

## Environment

**LAMP stack**
*	php >=7.1
*	MySQL >=5.7
*	Apache >=2.2
*	mod_rewrite


## Installation

Arrange Apache virtual host - level 1 domain or subdomain, not a level 2+ folder

`cd /target/folder`

`git clone https://github.com/sarapis/fusio-orapi .`

`mysql -u root -p < fusio-orapi.sql`

`composer update`



Enter server url into .env file located at _/target/folder/.env_

ex: `FUSIO_URL="http://example.com"`



## API

API is available for reading data from several entry points described by Human Service Data API Suite (HSDA) - https://openreferral.readthedocs.io/en/latest/hsda/

Base API entry point is /

Authentication is not required



API docs available at /developer


## API back-end

/fusio/#!/login

user: fusio-orapi-user

pass: Openreferral123changethis++


## MySQL

During the installation two databases and service user will be created:
* DB `openreferral_data` - containing main HSDA dataset
* DB `openreferral_fusio` - containing management information for API



user: fusio-orapi-user

pass: Openreferral123changethis++


If you need to change DB names or credentials you have to update 
* .env file located at _/target/folder/.env_
* Connection &gt; Mysql_HSDA parameters at API back-end