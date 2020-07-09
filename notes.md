# Chapter 1

## Creating Project
```
django-admin startproject project_name
```

## Running Project
```
python manage.py runserver
```

## Creating an app

```
python manage.py startapp app_name
```

## Views

Inside views to simply response the plain text, simply import the HttpResponse from http package like:

```
from django.http import HttpResponse


def index(request):
	return HttpResponse("Hello, world")
```

## Routing Utilities

After creating an app, you need to create a urls.py inside file in order to separate the route.
The urls file needs to import path from urls like:

```
from django.urls import path
```

Import the views like:

```
from . import views
```

And use path inside predefined variable **urlpatterns** to describe the necessary route like:

```
urlpatterns = [
	path('', views.index, name='index')
]
```

## Including Separate Route To Main Route

First import the include from urls package 
```
from django.urls import include
```

Then include it like:

urlpatterns = [
	path('polls', include('polls.urls'))
]
