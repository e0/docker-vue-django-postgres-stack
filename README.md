# Docker starter kit with Vue, Django REST framework, and PostgreSQL
Download this repo and rename it after your project.

Modify: `project.sh`, replace `<PROJECT NAME>`

Modify: `frontend/packge.json`

`source proj.sh`

`bootstrap`

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

`start-stack`

