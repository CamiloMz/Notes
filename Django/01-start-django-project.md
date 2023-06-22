# Start a new Django Project
This documents describes how to install, create and run your first Django project.

## Table of Contents

- [Install Django](#install-django).
- [Create a Django Project](#create-a-django-project).
- [Run a dev-server](#run-a-dev-server).

## Install Django

1. Create a virtual environment.

    ```shell
    python -m venv venv
    ```

2. Install Django.
    
    ```shell
    python -m pip install Django
    ```

3. Check the Django installation.
    
    ```shell
    python -m django --version
    ```

## Create a Django Project

1. Create a project.
    
    ```shell
    django-admin startproject mysite
    ```

## Run a dev-server

1. Run a dev server.
    
    ```shell
    python manage.py runserver
    ```

2. Go to [http://localhost:8000/](http://localhost:8000/).