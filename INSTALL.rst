============
Installation
============

Add to your project's requirements.txt::

    -e git://github.com/audreyr/django-regplus#egg=django-regplus

Add to INSTALLED_APPS in your project's settings.py::

    INSTALLED_APPS = [
        ...
        'regplus',
    ]

Also add to your project's settings.py::

    ACCOUNT_ACTIVATION_DAYS = 2
    EMAIL_HOST = 'localhost'
    DEFAULT_FROM_EMAIL = 'webmaster@localhost'
    LOGIN_REDIRECT_URL = '/'

Add to your project's urls.py::

    url(r'^accounts/', include('registration.urls')),

Now syncdb and runserver::

    python manage.py syncdb
    python manage.py runserver

You should now be done.  Open a web browser to http://127.0.0.1:8000/accounts/register/ and try registering. 

