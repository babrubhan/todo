# todo

1. Create an application
   $ django-admin startproject projectname

2. Edit a file  "mysite/mysite/settings.py"
      ALLOWED_HOSTS = ['*']
      
3. Creating the application
      $ python3 manage.py startapp todo
      
4. Edit the settings file("mysite/mysite/settings.py") to add "todo.apps.TodoConfig" to the INSTALLED_APPS list.

      INSTALLED_APPS = [
    'todo.apps.TodoConfig',
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    ]
    
5. Run the server
        $ python3 manage.py runserver
        
6. Create Database
        $ sudo systemctl enable mysql
        $ sudo systemctl start mysql
        
       $ mysql -u root
      create database mydb;
      
7. Open and edit the file to change database engine from SQLite to MySQL. Don't forget to add "import pymysql",              "pymysql.install_as_MySQLdb()" to use the MySQL
 
      import pymysql
      pymysql.install_as_MySQLdb()

      DATABASES = {
       'default': {
         'ENGINE': 'django.db.backends.mysql',
         'NAME': 'mydb',
         'USER': 'USERNAME',
         'PASSWORD': 'PASSWORD',
         'HOST': '127.0.0.1',
         'PORT': '3306',
          }
        }
      
 8. Create Superuser
        $ python3 manage.py createsuperuser
          
 9. Creating HTML template
        - see the files in the directory: "mysite/todo/templates"
        
 10. Run the application
