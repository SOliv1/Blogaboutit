# Django Blog Mini Project

## A simple blog app usig Django

`pip3 install django==1.11.29`

`pip freeze > requirements.txt`

`django-admin startproject blog .`

`pip3 install django`

`python3 manage.py migrate`

`python3 manage.py runserver`

`git init`

`.gitignore`
ignore all unwanted files below with following command:
`echo -e "*.db.sqlite3\n*.pyc\n_pycache_/" > .gitignore`

`python3 manage.py startapp posts`

`pip3 install pillow`   for images

`pip3 freeze > requirements.txt`

`python3 manage.py makemigrations`

`django-forms-bootstrap` 
and add this to installed apps in settings.py as django_forms_bootstrap underscores.

`python3 manage.py createsuperuser`
## csrf_token
So let's return to our CSRF token.
This is a protection mechanism provided by Django to make sure that your website isn't vulnerable to cross-site request forgery attacks.
Now, you can read more about that on the Internet if you want.
Bootstrap takes care of this under the bonnet, so we don't have to.
But it's a very good practice to remember to include csrf_token in every form that we create.

login to admin
admin
admain@project.com
Blogsgalore

## Heroku
*Procfile*
*requirements.txt*

Heroku login
Dashboard go to create new app
settings page
fill in the environmental vairables
go to rescources and type in searchbox for **Heroku Postgres*
click on create new database - hobbydevelopment freeze
add secret key from env.py to environment variables in config variables
add the localhost 


`pip3 install dj-database-url psycopg2`  : connects our database to our urls

`pip3 freeze > requirements.txt` again to update requirements.txt


Comment out default database and create a new database dictionary not a string:

DATABASES = {
    'default': dj_database_url.parse(os.environ.get('DATABASE_URL'))
}

and then scroll to the top of setting.py to import it.
import dj_database_url

Collect the database url from postgres on heroku vars and add for local testing purposes only they will not go live.
and paste in the env.py file.
os.environ.setdefault(),

now we should be able to deploy:
`python3 manage.py makemigrations`


[![Build Status](https://travis-ci.com/SOliv1/Blogaboutit.svg?branch=master)](https://travis-ci.com/SOliv1/Blogaboutit)
