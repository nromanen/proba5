Docker compose in github actions

We have web application. This application use Flask framework and redis store.

Create a Dockerfile. 
In this file required variables are :

FLASK_APP with value of home.py

FLASK_RUN_HOST with value of server address (localhost).

For runing this application locally we should to do such steps:

* install python 3.7

* execute command pip install -r requirements.txt

* flask run

Create docker-compose file with two services:

* `web` with container_name app which builds Dockerfile in the root of the project

* `redis` which pulls redis image from the docker hub
