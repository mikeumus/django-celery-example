### Code Playground at C9 - https://ide.c9.io/mikeumus/celery-django-example

##### Celery Processes Notes
- Celery + Django Project Template by @dvl: https://github.com/dvl/celerytest 
 - Thanks @dvl :)
 - and celery docs django template: https://github.com/celery/celery/tree/3.1/examples/django
- Retry Policy
 - http://docs.celeryproject.org/en/master/userguide/calling.html#retry-policy 
- Starting tasks in the background with `celery multi`: http://docs.celeryproject.org/en/master/getting-started/next-steps.html?highlight=multi#in-the-background
 - `celery multi start w1 -A proj -l info`
 - Starting a process locally in the terminal: `celery -A proj worker -l info`

_ _ _


     ,-----.,--.                  ,--. ,---.   ,--.,------.  ,------.
    '  .--./|  | ,---. ,--.,--. ,-|  || o   \  |  ||  .-.  \ |  .---'
    |  |    |  || .-. ||  ||  |' .-. |`..'  |  |  ||  |  \  :|  `--, 
    '  '--'\|  |' '-' ''  ''  '\ `-' | .'  /   |  ||  '--'  /|  `---.
     `-----'`--' `---'  `----'  `---'  `--'    `--'`-------' `------'
    ----------------------------------------------------------------- 


Welcome to your Django project on Cloud9 IDE!

Your Django project is already fully setup. Just click the "Run" button to start
the application. On first run you will be asked to create an admin user. You can
access your application from 'https://celery-django-example-mikeumus.c9.io/' and the admin page from 
'https://celery-django-example-mikeumus.c9.io/admin'.

## Starting from the Terminal

In case you want to run your Django application from the terminal just run:

1) Run syncdb command to sync models to database and create Django's default superuser and auth system

    $ python manage.py syncdb

2) Run Django

    $ python manage.py runserver $IP:$PORT
    
## Support & Documentation

Django docs can be found at https://www.djangoproject.com/

You may also want to follow the Django tutorial to create your first application:
https://docs.djangoproject.com/en/1.7/intro/tutorial01/

Visit http://docs.c9.io for support, or to learn more about using Cloud9 IDE.
To watch some training videos, visit http://www.youtube.com/user/c9ide