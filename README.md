# pytonik .env file setup

[pytonik](https://pypi.python.org/pypi/pytonik) .env file contains properties with parameters that enable the deployment and development of web application using [pytonik](https://pypi.python.org/pypi/pytonik) frame work.
[pytonik](https://pypi.python.org/pypi/pytonik) MVC cannot run or function without setting all necessary parameters.

## .env Property
  - route
  - dbConnect
  - languages
  - error
  - SMTP

## route
route set all default method for reused purposes, either to pass on parameters or revoking controller, below is the illustration, we'll be using ContactController 
```
'route':
        {
         'contact/edit' : 'ContactController@edit',
         'contact/add' : 'ContactController@add'
        }
```

Define default language

```
'default_languages':'en'
```

Note: **edit** and **add** are functions in **ContactController** module

## dbConnect
dbConnect set all Database connection parameters, configure pytonik to work with MYSQL database, parameters are required to enable database to function probably  

### MYSQLi
```
'dbConnect':
         {
              'host': 'localhost',
              'database': 'pytonik-database',
              'password': 'database-password',
              'username': 'database-username',
              'port': 'database-port',
              'driver': 'MYSQL'
         }
``` 

**MYSQLi**  requires mysql-connector-python module

```
$ pip install mysql-connector-python

``` 


### SQLite

```
'dbConnect':
         {
              'path': 'Folder-name',
              'name': 'database-file-name',
              'driver': 'SQLite'
         }
``` 

**Note:** driver support only **SQLite** and  **MYSQLi**  Database


## languages
Enable pytonik application to run multiple language translation, all language dictionary file are created in **lang** folder 
```
'languages':
{
   'en': '',
   'fr': '',
   'ef': '',
}
```

Define default language

```
'default_languages':'en'
```
**Note:** default language is compulsory

## SMTP
Enable  application to send mails to or fro pytonik
```
'SMTP':
{
    'server':   'test@server.com',
    'port':     '25',
    'username': 'test@example.com',
    'password': 'testpassword',
}
```
**Note:** Application that requires sending of mails, above setup is compulsory


## default
Define all default **routes** , **controllers** , **action** and **language** when developing or deploying a standard  application

```
'default_actions': '',
'default_controllers' :'',
'default_routes' : '',
'default_languages':''
```


pytonik is open to questions, feel free to ask.

## Contact Information: 

**Name:**  pytonik MVC

**Email:** pytonikmvc@gmail.com

