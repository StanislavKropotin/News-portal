# News-portal
Django project.
A small news portal implemented registration via Yandex, or with confirmation via email (using the django-allauth package).
Models.py describes the classes Author, Category, Post, PostCategory, Comment, Subscriptions and the relationships between them.
A censor filter has been written that replaces the letters of some words in the titles and texts of articles with the “*” symbol.
Pagination done (10 per page).
Added the ability to search for an article by title, author, date and category.
Authors and administrators can delete/create/edit publications. A regular user cannot.
The template is based on Bootstrap.
The user has the ability to subscribe and unsubscribe to categories.
I connected Django with Redis and Celery, and with their help I implemented sending letters to subscribers of certain categories to their registered email when creating a new publication (asynchronously).
Implemented weekly sending of subscriber letters once a week (on Mondays, at 8:00 am).
I did caching.


What to do to make it work:

Dependencies need to be installed (pip install -r requirements.txt)

Run the command python manage.py runserver

Follow the link http://127.0.0.1:8000/post/

News can be created directly through the application. It is enough to create a superuser, or simply register
