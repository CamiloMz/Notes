# Django
This documents shows hot to setup the database.

## Table of Contents

- [Database setup](#database-setup).
- [Create models](#create-models).
- [Activating models](#activating-models).
- [NOTES](#notes).

## Database setup


1. Install the appropriate database bindings and change the following keys in the DATABASES 'default' item to match your database connection settings:

    *   **ENGINE** – Either 'django.db.backends.sqlite3', 'django.db.backends.postgresql', 'django.db.backends.mysql', or 'django.db.backends.oracle'.

    *   **NAME** – The name of your database. NAME should be the full absolute path, including filename, of that file. 


    ```python
        DATABASES = {
            'default': {
                "ENGINE": "django.db.backends.postgresql",
                "NAME": "mydb",
                "USER": "myuser",
                "PASSWORD": "myuserpassword",
                "HOST": "127.0.0.1", ## Default
                "PORT": "5432", ## Default
                'ATOMIC_REQUESTS': True,
            }
        }
    ```

2. Create the tables in the database before you can use the **``INSTALLED_APPS``**.
    ```shell
    python manage.py migrate
    ```

    if you have problems run:
    ```shell
    pip install psycopg2-binary --force-reinstall --no-cache-dir
    ```



## Create models

1. Create a model in myapp editing myapp/models.py.
    
    ```python
    from django.db import models


    class Person(models.Model):
        first_name = models.CharField(max_length=30)
        last_name = models.CharField(max_length=30)
    ```

## Activating models

1. Tell your project that myapp is installed. Add a reference to its configuration class in the INSTALLED_APPS setting.  The MyAppConfig class is in the myapp/apps.py file, so its dotted path is 'myapp.apps.PollsConfig'. Edit the mysite/settings.py file and add that dotted path to the INSTALLED_APPS setting.
    
    ```python
    INSTALLED_APPS = [
        "myapp.apps.MyAppConfig",
        "django.contrib.admin",
        "django.contrib.auth",
        "django.contrib.contenttypes",
        "django.contrib.sessions",
        "django.contrib.messages",
        "django.contrib.staticfiles",
    ]
    ```


2. Tell Django that you’ve made some changes to your models (in this case, you’ve made new ones) and that you’d like the changes to be stored as a migration.
    
    ```shell
    python manage.py makemigrations myapp
    ```
    You can also ``run python manage.py check``; this checks for any problems in your project without making migrations or touching the database.

3.  See what SQL that migration would run. The sqlmigrate command takes migration names and returns their SQL:

     ```shell
    python manage.py sqlmigrate polls 0001
    ```

4.  Run ``migrate`` again to create those model tables in your database.

    ```shell
    python manage.py migrate
    ```

# NOTES:

Remember the three-step guide to making model changes:

* Change your models (in models.py).

* Run python manage.py makemigrations to create migrations for those changes.

*Run python manage.py migrate to apply those changes to the database.