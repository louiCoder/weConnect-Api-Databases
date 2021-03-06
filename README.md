[![Build Status](https://travis-ci.org/louiCoder/weConnect-Api-Postgres-Database.svg?branch=develop)](https://travis-ci.org/louiCoder/weConnect-Api-Postgres-Database)
[![Maintainability](https://api.codeclimate.com/v1/badges/b4e864ea0427cfb100a8/maintainability)](https://codeclimate.com/github/louiCoder/weConnect-Api-Postgres-Database/maintainability)
[![Coverage Status](https://coveralls.io/repos/github/louiCoder/weConnect-Api-Postgres-Database/badge.svg)](https://coveralls.io/github/louiCoder/weConnect-Api-Postgres-Database)


# weConnect-Api-Databases

WeConnect-Api provides a platform that brings businesses and individuals together. This platform creates awareness for businesses and gives the users the ability to write reviews about the businesses they have interacted with.

## _Author_:
    Louis Musanje Michael

## __Project captures the following routes__

| REQUEST | ROUTE | FUNCTIONALITY |
| ------- | ----- | ------------- |
| POST | /api/auth/register | creating user account |
| POST | api/auth/login | logging in for a user |
| POST | api/auth/logout | Logs out a user |
| POST | api/auth/reset-password | Password reset |
| POST | api/businesses | Registering a business |
| PUT | api/businesses/<_businessId_>| Updating a business profile |
| DELETE | api/businesses/<_businessId_>| delete/remove a business profile |
| GET | api/businesses | gets all avaliable businesses |
| GET | api/businesses/<_businessId_>| Get a business |
| POST | api/businesses/<_businessId_>/reviews | Add a review for a business |
| GET | api/businesses/<_businessId_>/reviews | Get all reviews for a business |


### __Technologies used to develop and test this app__
1. Python
2. Postgresql DBMS
3. Postman
4. VSCODE (for editing and debugging)

### __Project dependencies will always be found in the file below__
    requirements.txt

### __Set up project to get it up and running__
* clone repository from link below
  
      $ git clone https://github.com/louiCoder/weConnect-Api-Postgres-Database.git
* Set up Virtual environment by running commands below

      * virtualenv venv
      * source /venv/Scripts/activate (for linux/mac)
      * /venv/Scripts/activate.exe (for windows)

* Get all project dependencies by running the command below.

      $ pip freeze -r requirements.txt

### Set up postgres database

      $ sudo -u postgres createuser --interactive
      $ sudo -u postgres createdb <database_username> 

### connect to postgres database 
      $ sudo -u <database_username> psql
      $ psql -d postgres

### set up environment variables

      $ APP_SETTINGS="config.TestingConfig" or "config.ProductionConfig" or "config.DevelopmentConfig"
      $ DATABASE_URL="postgres://<username_>_password_ @localhost/database_name"

### run the migrations 
      $ python manage.py shell
      $ db.create_all()
      $ exit()
      $ python manage.py db init
   
### To run the unit tests invoke/run the command below.

      $ nosetests tests 

### or for detailed output on unit tests run with verbose.

      $ nosetests -v tests
      
### To run the application invoke the command below.

      $ python manage.py runserver
      
### Now that the server is running , open your browser and run one of the links below.

      $ localhost:5000  or  127.0.0.1:5000

### Access the apidocs with the caddress below
      $ localhost:5000/apidocs  or  127.0.0.1:5000/apidocs

### To access the apidocs direct run gunicorn server with command below
      $ gunicorn
