# Flask App

The following project was built during my course with Bottega. It has full CRUD functionality.

> Dependencies Documentation
- FLASK
  - http://flask.palletsprojects.com/en/1.1.x/
- FLASK-MARSHMALLOW
  - https://flask-marshmallow.readthedocs.io/en/latest/
- FLASK-SQLALCHEMY
  - https://flask-sqlalchemy.palletsprojects.com/en/2.x/
- MARSHMALLOW-SQLALCHEMY
  - https://marshmallow-sqlalchemy.readthedocs.io/en/latest/


### Commands to follow after downloading
- Install all the dependencies
```
$ pipenv install
```

### Create Database
- If you need to create a database. Hop into a python repl and run the following commands.
- When you're done you should have an app.sqlite file. That file will be your database.
```
>>> from app import db
>>> db.create_all()
```

### Starting your server
- Enter a pipenv shell first
```
$ pipenv shell
```
- Start the server
```
$ python app.py
```


### How to run queries

  - POST a Guide
  ```
  Route: localhost:5000/guide
  Method: POST
  body: {
    "title": "some content"
    "content": "some content"
  }
  content-type: JSON
  ```

  - GET all Guides
  ```
  Route: localhost:5000/guides
  Method: GET
  ```
  - GET a single guide
  ```
  - The id will be dynamic. You will put in the id for the guide that you want to collect from the database.
  Route: localhost:5000/guide/id
  Method: GET
  ```
  - PUT a single guide
  ```
  - The id will be dynamic. You will put in the id for the guide that you want to edit from the database.
  Route: localhost:5000/guide/id
  Method: PUT
  body: {
    "title": "Updated content"
    "content": "Updated content
  }
  content-type: JSON
  ```
  - DELETE a single guide
  ```
  - The id will be dynamic. You will put in the id for the guide that you want to delete from the database.
  Route: localhost:5000/guide/id
  Method: DELETE
  ```