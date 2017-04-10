# Flask Blog

First version was created using https://github.com/mjhea0/flaskr-tdd tutorial. Good one!!

## Notes

* I pulled off heroku deployment, since I won't use it. **But gunicorn part was usefull**

* I don't frozen Flask-SQLAlchemy to a version. it leads to intall a old 1.1.9 version.
The newest version was 2.2 when i tested.

* to correct warnings, I needed to replace the line in app.py

```
from flask.ext.sqlalchemy import SQLAlchemy
```


for
```
from flask_sqlalchemy import SQLAlchemy
```

* At configuration of database section, from :

```
# the database uri
SQLALCHEMY_DATABASE_URI = 'sqlite:///' + DATABASE_PATH
```

to


```
# the database uri
SQLALCHEMY_DATABASE_URI = 'sqlite:///' + DATABASE_PATH
#eliminates a warning. Set to false when don't need, since adds overhead.
SQLALCHEMY_TRACK_MODIFICATIONS = True

```



The good points are this tutorial apresent some minimal decent structure to work with
flask, with JQuery, bootstrap, SQLAlchemy, git and some configuration to use gunicorn.

The bad point are:
* the deployment to heroku is not enough to every developer scenario,
and gunicorn use is incomplete if not used in heroku.
* The method to delete posts works even when not logged, and is not intuitive.
* It haven't comments




