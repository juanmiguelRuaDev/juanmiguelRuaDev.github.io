---
layout: post
title:  "Snippets Django"
image: ''
date:   2017-10-09 00:06:31
tags:
- django
- python
- snippets
description: 'This is my firts post: Django snippets'
categories:
- Snippets
serie: learn
---

<img src="{{ "/assets/img/2017-02-25/django-logo-positive.png"}}">


## Introduction

This entry aims to collect all the helpful command that I always forget, but are essential to build a django project from scratch.

We'll assume that you have [Django installed](https://docs.djangoproject.com/en/1.11/intro/install/) already and you have strong knowledge of python. More concretely `python v3.x`.

The information showed here has been taken from the [official Django webpage](https://docs.djangoproject.com/en/1.11/) 



## Index

1 [create the site](#create-site)

2 [Run the server](#run-the-server)

3 [Create an app](#create-an-app)

4 [Collect static](#collect-static)

5 [Data base operations](#database-operations)




### Create site
_source:_ [https://docs.djangoproject.com/en/1.11/intro/tutorial01/](https://docs.djangoproject.com/en/1.11/intro/tutorial01/)
{% highlight bash %}
$ django-admin startproject mysite
{% endhighlight %}



### run the server

_source:_ [https://docs.djangoproject.com/en/1.11/intro/tutorial01/](https://docs.djangoproject.com/en/1.11/intro/tutorial01/)
{% highlight bash %}
$ python manage.py runserver
{% endhighlight %}



### create an app

_source:_ [https://docs.djangoproject.com/en/1.11/intro/tutorial01/](https://docs.djangoproject.com/en/1.11/intro/tutorial01/)


{% highlight bash %}
$ python manage.py startapp app
{% endhighlight %}




### Collect static

The first time that I created any static file in my project, I thought that it was enough. I was wrong, you have to run the following script to move either the new and modified static files to the path defined in your config file.

{% highlight bash %}
python3 manage.py collectstatic --settings "project.settings"
{% endhighlight %}


### Database operations

I always forget what are the scripts to migrate any change in database. 

1. Make migration

{% highlight bash %}
python manage.py makemigrations <appname>
{% endhighlight %}

2. Migrate from specified point number

{% highlight bash %}
python manage.py sqlmigrate <appname> 000x
{% endhighlight %}

3. Check for any problem in your project

{% highlight bash %}
python manage.py check
{% endhighlight %}

4. Migrate all changes executing the SQL sentences

{% highlight bash %}
python manage.py migrate
{% endhighlight %}
