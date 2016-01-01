# sof1231

Hello SOF,

I am new to django and I misunderstand how to use templates.

I have a a file called base.html which I see as a parent to hello.html.

In hello.html I have this syntax:

{% extends "base.html" %}

```
{% extends "base.html" %}

{% block hello %}
<h1>hello</h1>
I should see this template. This is the hello.html template.
{% endblock %}
```

In base.html I have this syntax:

{% block hello %}{% endblock %}

It is my understanding that django should render hello.html inside of base.html

When I deploy my two html files, django ignores my syntax.

Question: How to render hello.html in base.html?

The files are visible inside of github:



# python-getting-started

A barebones Python app, which can easily be deployed to Heroku.

This application support the [Getting Started with Python on Heroku](https://devcenter.heroku.com/articles/getting-started-with-python) article - check it out.

## Running Locally

Make sure you have Python [installed properly](http://install.python-guide.org).  Also, install the [Heroku Toolbelt](https://toolbelt.heroku.com/) and [Postgres](https://devcenter.heroku.com/articles/heroku-postgresql#local-setup).

```sh
$ git clone git@github.com:heroku/python-getting-started.git
$ cd python-getting-started
$ pip install -r requirements.txt
$ createdb python_getting_started
$ heroku local:run python manage.py migrate
$ python manage.py collectstatic
$ heroku local
```

Your app should now be running on [localhost:5000](http://localhost:5000/).

## Deploying to Heroku

```sh
$ heroku create
$ git push heroku master
$ heroku run python manage.py migrate
$ heroku open
```
or

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Documentation

For more information about using Python on Heroku, see these Dev Center articles:

- [Python on Heroku](https://devcenter.heroku.com/categories/python)
