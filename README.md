# Docker starter kit with Vue, Django REST framework, and PostgreSQL
Download this repo and rename it after your project.

Modify: `project.sh`

Modify: `frontend/packge.json`

Create main backend django app: `docker-compose run backend django-admin.py startproject <PROJECT NAME> .`

Edit `backend/<PROJECT NAME>/settings.py`, replace the `DATABASES = …` section with:

```python
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

`docker-compose build`

`docker-compose up`

