# This is a cloneable boilerplate for django & tailwind. 

A few steps are needed to get up & running. 
- Install requirements by running `pip install django-heroku --no-deps && pip install -r requirments.txt`
- Install tailwind by running `python manage.py tailwind install`
- Change Project Name
1. Rename the `oldprojectname` directory to `newprojectname`
2. `manage.py`: Change `os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'oldprojectname.settings')`
3. `newprojectname/wsgi.py`: Change `os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'oldprojectname.settings')`
4. `newprojectname/settings.py`: Change `ROOT_URLCONF = 'oldprojectname.urls'` and change `WSGI_APPLICATION = 'oldprojectname.wsgi.application'`
5. `Procfile`: Change `web: gunicorn oldprojectname.wsgi` 
