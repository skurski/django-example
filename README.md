## Guide

### Installation

- Install PYTHON3 and PIP
- ```sudo pip install virtualenv ```
- Go to project directory (create if not exists)
- ```virtualenv -p python3 . ```
- ```source bin/activate ```
- ```pip install Django```

### Run project

- ```virtualenv -p python3 .```
- ```source bin/activate```
- ```python manage.py migrate```(run migrations for INSTALLED_APPS)
- ```python manage.py runserver host:port```(put host in /etc/hosts, by default 127.0.0.1:8000)

### Django commands

- ```python manage.py startproject mysite```
- ```python manage.py startapp polls```
- ```python manage.py shell```(python interactive shell)
- ```python manage.py createsuperuser``` (create admin account)

### Django Tests

- Create tests in tests.py file
- ```python manage.py test polls```

### Django db
- Register application in project settings (in INSTALLED_APPS)
- Make changes in model (in models.py)
- ```python manage.py makemigrations polls``` (create file with migrations for model)
- ```python manage.py sqlmigrate polls 0001``` (read and print content from file with migrations)
- ```python manage.py check``` (check for problems before running migration)
- ```python manage.py migrate``` (run migrations for INSTALLED_APPS)
- ```python manage.py dbshell``` (go to SQLITE shell)