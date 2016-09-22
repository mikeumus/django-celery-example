# Django-Celery Example
![django admin with django-celery tasks dashboard](https://0839a63ecb79fafd04ced14c58bd0806808b39ce.googledrive.com/host/0B9LVk4xbDIJTYmZXS2p3RVo0OXM)

⚠ Warning this was done in Dajngo 1.7 * 
_ _ _

#### Get Django-Celery Working!
1. Install [Python](https://www.python.org/downloads/) (if you're in linux, python 2.7 is already installed), [pip](https://pip.pypa.io/en/latest/installing.html), [django](https://docs.djangoproject.com/en/1.8/topics/install/) (and run `./manage.py syncdb`), [celery](http://www.celeryproject.org/install/), and django-celery
2. Choose your celery broker and install that: [RabbitMQ](http://celery.readthedocs.org/en/latest/getting-started/brokers/rabbitmq.html), [Redis](http://celery.readthedocs.org/en/latest/getting-started/brokers/redis.html), [others...](http://celery.readthedocs.org/en/latest/getting-started/brokers/)
3. Setup django-celery part 1: http://docs.celeryproject.org/en/latest/django/first-steps-with-django.html#using-the-django-orm-cache-as-a-result-backend
4. Setup django-celery part 2: https://github.com/celery/django-celery/blob/master/README.rst#using-django-celery
4. Start all the things (processes):
4. Start your `redis-server` or `rabbitmq-server`, ect...
5. Start Django: `./manage.py runserver` (and `./manage.py runserver $IP:$PORT` in Cloud 9)
6. Start the Celery Event Camera via: `./manage.py celery events --camera=djcelery.snapshot.Camera` 
7. Start `celeryd` with celery beat (`-B`): `./manage.py celeryd -B -l INFO`  
8. Run a task:
9. `./manage.py shell`
10. `from demoapp.tasks import add`
11. `add.delay(2,2)`
12. and you should then see things happening in the Celery Beat process and in the [Django Admin](https://docs.djangoproject.com/en/1.8/ref/contrib/admin/)

Lots of steps involved and that's why I put together this project to provide an isolated example of using django-celery that worked for me in 2015 on Django 1.7
The less steps it takes, the more likely you are to get it running sooner. Cheers!  

