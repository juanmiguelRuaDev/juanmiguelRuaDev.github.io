---
layout: post
title:  "Snippets Django"
image: ''
date:   2016-09-12 00:06:31
tags:
- django
- python
description: 'This is my firts post: Django snippets'
categories:
- Snippets
serie: learn
---

<img src="{{ "/assets/img/2017-02-25/mongodb-post.png"}}">

## Hello Post!

This is my first post, but I don't want to talk about me, I want to talk about technology, more concretly abut Django. I will post about me in future entries


## Collect static

The first time that I created any static file in my project, I thought that it was enough. I was wrong, you have to run the following script to move either the new and modified static files to the path defined in your config file.

{% highlight bash %}
python3 manage.py collectstatic --settings "project.settings"
{% endhighlight %}


## Data base operations

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
