# Docker starter kit with Vue, Django REST framework, and PostgreSQL
## Instructions (step per respective commit)
1. Starter kit.

2. Create app, update database configuration, run.

    `$ docker-compose run backend django-admin.py startproject <PROJECT NAME> .`

    Edit `backend/<PROJECT NAME>/settings.py`, replace the `DATABASES = ...` section with:

    ```
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql',
            'NAME': 'postgres',
            'USER': 'postgres',
            'HOST': 'db',
            'PORT': 5432,
        }
    }
    ```
    
    `$ docker-compose up`

3. Add frontend.
