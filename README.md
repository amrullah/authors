authors
=======

**Steps to install**

1. Clone this repo and create a virtualenv anywhere using `python3.6 -m venv {env_name}`
2. Activate the virtualenv and go to `authors/project` directory
3. Do `pip install -r requirements.txt`
4. Set these environment variables ```export DJANGO_SETTINGS_MODULE='config.settings' && export SECRET_KEY='{a random long string}'```
5. Ensure `postgresql-server` is running. You'll need to set following environment variables

...-DATABASE_NAME
...-DATABASE_USER
...-DATABASE_PASSWORD
...-DATABASE_HOST
...-DATABASE_PORT

6. Do `python manage.py migrate` to create all the tables in the database
7. Create a superuser account using `python manage.py createsuperuser`
7. Run the development server using `python manage.py runserver 0.0.0.0:8000`
8. In browser, go to `0.0.0.0:8000/admin` and log in using the superuser credentials you supplied above
9. In an another browser tab, go to `0.0.0.0:8000/documentation/` and see the list of all the REST API endpoints.
