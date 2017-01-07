## Guide

### Installation

- We need to have PYTHON3 and PIP installed on OS
- ```sh sudo pip install virtualenv ```
- Go to project directory (create if not exists)
- ```sh virtualenv -p python3 . ```
- ```sh source bin/activate ```
- pip install Django

### Run project

- ```sh virtualenv -p python3 .```
- ```sh source bin/activate```
- ```sh python manage.py migrate``` (run migrations for INSTALLED_APPS)
- ```sh python manage.py runserver host:port``` (put host in /etc/hosts, by default 127.0.0.1:8000)

### Django commands

- ```sh python manage.py startproject mysite```
- ```sh python manage.py startapp polls```
- ```sh python manage.py shell``` (python interactive shell)
- Create admin account:
	```sh python manage.py createsuperuser```

### Django Tests

- We create tests in tests.py file
- Run tests for given app:
	```sh python manage.py test polls```

### Django db
- Make changes in model (in models.py)
- If it is a new app with model we need to register it in project settings in INSTALLED_APPS
- Create file with migrations for change or new created models:
	```sh python manage.py makemigrations polls```
- Read and print content from file with migrations:
	```sh python manage.py sqlmigrate polls 0001```
- Check for problems before running migration:
	```sh python manage.py check```
- Run migrations for INSTALLED_APPS:
	```sh python manage.py migrate```
- Go to SQLITE command line:
	```sh python manage.py dbshell```