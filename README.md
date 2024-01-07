# django-tt
```
python3 -m venv my_env
source my_env/bin/activate
deactivate
django-admin startproject pr .

python manage.py runserver 9000
```
## django startpp
```
ctrl + shift + p
python manage.py startapp app
setting add app 
```
## 3.views
### /home/shah/sec/djtt/app/views.py
```
from django.shortcuts import render
from django.http import HttpResponse

def hello_world(request):
    return HttpResponse('hello world')
```
### /home/shah/sec/djtt/app/urls.py
```
from django.urls import path
from . import views

urlpatterns=[
    path('hello',views.hello_world)
]
```
### /home/shah/sec/djtt/prj/urls.py
```
from django.contrib import admin
from django.urls import path,include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('app/',include('app.urls'))
]
```
