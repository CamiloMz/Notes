# Django
This documents shows the process of creating and running your first app in Django.

## Table of Contents

- [Create an app for a Django Project](#create-an-app-for-a-django-project).
- [Write your first view](#write-your-first-view).
- [Create a URLconf](#create-a-urlconf).

## Create an app for a Django Project


1. Make sure you’re in the same directory as manage.py and type this command:

    ```shell
    python manage.py startapp myapp
    ```

## Write your first view

1. Open the file myapp/views.py and put the following Python code in it:
    
    ```python
    from django.http import HttpResponse


    def index(request):
        return HttpResponse("Hello, world. You're at the polls index.")
    ```

    To call the view, you need to map it to a URL, and for this you need a URLconf.

## Create a URLconf

1. Create a file called urls.py in myapp directory.
    
    ```shell
    myapp/
        __init__.py
        admin.py
        apps.py
        migrations/
            __init__.py
        models.py
        tests.py
        urls.py
        views.py
    ```

2. In the myapp/urls.py file include the following code:
    
    ```python
    from django.urls import path

    from . import views

    urlpatterns = [
        path("", views.index, name="index"),
    ]
    ```


3. Point the root URLconf at the myapp.urls module. In mysite/urls.py, add an import for django.urls.include and insert an include() in the urlpatterns list.
    
    ```python
    from django.contrib import admin
    from django.urls import include, path

    urlpatterns = [
        path("polls/", include("myapp.urls")),
        path("admin/", admin.site.urls),
    ]
    ```

4.  Go to [http://localhost:8000/myapp/](http://localhost:8000/myapp/).