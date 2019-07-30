# blogger

### Dev environment setup:
```bash
#in project directory:
virtualenv --python python3 envgrocer
source envgrocer/bin/activate
deactivate
```

### Django install:
```bash
#in virtualenv:
pip install Django==2.0.5
```

### Django validate and verify:
```bash
#in python3 shell
import django
django.get_version()
```

### Dependency management:
```bash
#pin depedencies in current project:
pip freeze > requirements.txt

#download dependencies when working in different environment:
pip install -r requirements.txt
```

### Add a django project
```bash
#create a project called blogger
django-admin startproject blogger
```
### Create tables in django database
```bash
#inside the project directory
cd blogger
python manage.py migrate
```

### Start the dev server at 127.0.0.1:8000
```bash
python manage.py runserver
```

### Clean up
```bash
lsof -nP -i4TCP:8000
kill -9 $PID
```

### Create an app:
```bash
python manage.py startapp blog
```

###When updating models:
```bash
#create a migration
python manage.py makemigrations blog
#sync database with new model
python manage.py migrate
```