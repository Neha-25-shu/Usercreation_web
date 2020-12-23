# Welcome to django web
  ===========================


Django packages provides a set of module  for user Registration Authentication and Authorization 

# Documentation
  -------------
  http://django-rest-auth.readthedocs.org/en/latest/


# Technology Stack We have used

1. Python 3.6
2. Django 3.1.2
3. Django REST Framework
4. sqlite3 Database
5. Google Chrome v.83.0.4103.61    
6. Google Chrome driver v.83.0.4103.61


# Project Structure:
 
    .
    ├── API.md : API documentation
    ├── README.md : documentation file
    └── registration
        ├── core
        │   ├── admin.py
        │   ├── apps.py
        │   ├── forms.py
        │   ├── models.py: database models for core app
        │   ├── __init__.py
        │   ├── migrations : database migrations
        │   │   ├── __init__.py
        │   ├── tests.py: test cases for view
        │   ├── urls.py : urls for core app
        │   └── views.py: These views are called by url name
        ├── db.sqlite3: databse 
        ├── django_user
        │   ├── __init__.py
        │   ├── settings.py : settings file for the project.
        │   ├── urls.py : base urls for apps of the projects
        │   └── wsgi.py
        ├── manage.py
        ├── requirements.txt : requirements needs to be install
        └── templates
            ├── base.html
            ├── commons
            │   ├── change-password.html
            │   ├── login.html
            │   ├── password-reset
            │   │   ├── password_reset_complete.html
            │   │   ├── password_reset_confirm.html
            │   │   ├── password_reset_done.html
            │   │   ├── password_reset_email.html
            │   │   ├── password_reset.html
            │   │   └── password_reset_subject.txt
            │   ├── profile.html
            │   └── signup.html
            ├── home.html
            └── registration
                └── login.html
	

# Features:
  ---------
  * User registration

  * User email verification

  * Change password - with password reset email.
  
  * Users profile 
  

## APIs Details

   See documentation [here.](./API.md)
  
  
## Run the project Locally ##

i. Clone the repository.

ii. Go to directory of manage.py and install the requirements.

	pip install -r requirements.txt
	
**Note:**
You may configure the virtual environment if required.

For instructions, click here : https://virtualenv.pypa.io/en/latest/installation/
    


**Note:**
By default, dbSqlite3 database is used. You may also use different database in local_settings file if required.

iii. Run migrations

	    python manage.py migrate

iv. Ready to run the server.

	  python manage.py runserver


# Linting:

	make lint


# Testing:

	python manage.py test
  
  
