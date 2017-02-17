# Docker starter kit with Vue, Django REST framework, and PostgreSQL
Download this repo and rename it after your project.

Add a `postgres.env` file based on the `postgres.env.sample` file:

```bash
$ cp postgres.env.sample postgres.env
```

Modify the `postgres.env` 

Modify: `project.sh`, replace `<PROJECT NAME>`

Modify: `frontend/packge.json`

`$ source proj.sh`

`$ bootstrap`

Edit `backend/<PROJECT NAME>/settings.py`, replace the `DATABASES = …` section with:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': os.getenv('POSTGRES_DB'),
        'USER': os.getenv('POSTGRES_USER'),
        'PASSWORD': os.getenv('POSTGRES_PASSWORD'),
        'HOST': 'db',
        'PORT': 5432,
    }
}
```

Append the following into the `INSTALLED_APPS` section of the same file:

```
    'rest_framework',
    'api',
```

`$ start-stack`

