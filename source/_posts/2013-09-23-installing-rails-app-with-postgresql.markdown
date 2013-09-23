---
layout: post
title: "Installing rails app with postgreSQL"
date: 2013-09-23 00:56
comments: true
categories: rails,ruby, postgreSQL

---

I've been working on the backend side of rails apps the past few months. One thing I've realized
is that you can go through a million tutorials but until you put those concepts to work you'll have
a harder time grasping them.

Today I want to go over a very simple concept. This is applicable in many ways, especially when learning
to use different databases in a rails app. Today we'll be covering installing a brand new rails app with
the postgreSQL database. Normally you'd have the SQLite db set up by default. There are numerous advantages
to this.. one being that heroku uses this... and if you're installing your apps on heroku its nice to be
using the same database as heroku to avoid any potential issues that could come up relating to database configuration.

#Okay on to business...


{% codeblock Time to be Awesome %}
rails new yourApp --database=postgresql
{% endcodeblock %}

That's it. If you already have a rails app created and want to switch its still very straightforward.

1 Remove the sqlite gem from your gemfile
2 Add in the gem 'pg' into your gemfile
3 run bundle
4 Then make sure your database.yml files are using the correct adapters. Here is an example
{% codeblock Time to be Awesome %}
development:
  adapter: postgresql
  encoding: unicode
  database: appname_development
  pool: 5
  username: your_system_username
  password:
{% endcodeblock %}
That's it. You should be good to go. Of course you'll need to make sure you have the PG installed on your system.
If you have homebrew you can do this easily

{% codeblock Time to be Awesome %}
  $ brew update
  $ brew doctor
  $ brew install postgresql
{% endcodeblock %}


The first two commands make sure brew is up to date and healthy... the third is the command to install postgreSQL. That's it.
This is something I would have found useful a few months ago so I figured I would include it here.


Enjoy and Be Awesome

