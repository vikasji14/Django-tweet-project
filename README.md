<!-- step 1 -->
# create env file  
python -m venv .venv
# to activate the virtual environment 
.venv\Scripts\activate

<!-- step 2 -->
# to install Django
 pip install django


<!-- step 3 -->
# pip freeze
 pip freeze > requirements.txt    


<!-- step 4 -->
# To create a new Django project
 django-admin startproject <projectname>


<!-- step 5-->
# Migrate
 python .\manage.py migrate


<!-- step 6 -->
# Start a Django Server
 python manage.py runserver


<!-- step 7 -->
# Django admin 
 python .\manage.py createsuperuser


<!-- step 8 -->
# setting.py
 import os

# media url
 MEDIA_URL = '/media/'
 MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
# static
 STATIC_URL = 'static/'
 STATICFILES_ROOT = os.path.join(BASE_DIR, 'static')

<!-- step 9 -->
# urls.py
 from django.contrib import admin
 from django.urls import path
 from django.conf import settings
 from django.conf.urls.static import static

 urlpatterns = [
    path('admin/', admin.site.urls),



 ]+ static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)



<!-- step 10 -->
# create new app
 python manage.py startapp <appname>
 create - urls.py 
 go to setting.py file and write under
 INSTALLED_APPS = [
    '<appname>'                   # tweet
 ]
 Tamplates
 'DIRS': [os.path.join(BASE_DIR, 'templates')],


 # migrations
  python .\manage.py makemigrations <appname>









  


  
