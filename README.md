# Django-Celery Example
![django admin with django-celery tasks dashboard](https://0839a63ecb79fafd04ced14c58bd0806808b39ce.googledrive.com/host/0B9LVk4xbDIJTYmZXS2p3RVo0OXM)

_ _ _

#### Get Django-Celery Working!
1. Install [Python](https://www.python.org/downloads/) (if you're in linux, python 2.7 is already installed), [pip](https://pip.pypa.io/en/latest/installing.html), [django](https://docs.djangoproject.com/en/1.8/topics/install/) (and run `./manage.py syncdb`), [celery](http://www.celeryproject.org/install/), and django-celery
2. Choose your celery broker and install that: [RabbitMQ](http://celery.readthedocs.org/en/latest/getting-started/brokers/rabbitmq.html), [Redis](http://celery.readthedocs.org/en/latest/getting-started/brokers/redis.html), [others...](http://celery.readthedocs.org/en/latest/getting-started/brokers/)
3. Start all the things (processes):
 3.1 Start your `redis-server` or `rabbitmq-server`, ect...
 3.2 Start Django: `./manage.py runserver` (and `./manage.py runserver $IP:$PORT` in Cloud 9)
 3.4 Start the Celery Event Camera via: `./manage.py celery events --camera=djcelery.snapshot.Camera` 
 3.4 Start `celeryd` with celery beat (`-B`): `./manage.py celeryd -B -l INFO`  
4. Run a task:
 4.1 `./manage.py shell`
 4.2 `from demoapp.tasks import add`
 4.3 `add.delay(2,2)`
5. and you should then see things happening in the Celery Beat process and in the [Django Admin](https://docs.djangoproject.com/en/1.8/ref/contrib/admin/)

_ _ _

### Code Playground at C9
https://ide.c9.io/mikeumus/celery-django-example

##### Celery Processes Notes
- Starting tasks in the background with `celery multi`: http://docs.celeryproject.org/en/master/getting-started/next-steps.html?highlight=multi#in-the-background
 - `./manage.py celery multi start w1 -A proj -l info`
 - Starting a process locally in the terminal: `./manage.py celery -A proj worker -l info`
 - Starting event camera: `./manage.py celery events --camera=djcelery.snapshot.Camera`

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