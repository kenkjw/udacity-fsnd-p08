# Udacity Full Stack Nanodegree Project: Linux Server Configuration

## Project Description:
From the Udacity course:
You will take a baseline installation of a Linux distribution on a virtual machine and prepare it to host your web applications, to include installing updates, securing it from a number of attack vectors and installing/configuring web and database servers.


## Server Information:
- IP address: 35.161.102.45
- URL: [http://ec2-35-161-102-45.us-west-2.compute.amazonaws.com/](http://ec2-35-161-102-45.us-west-2.compute.amazonaws.com/)

## Summary of software installed:
- From Apt-get
    - Git - version control system that is used for software development and other version control tasks
    - Apache2 - Web Server software
    - Postgresql - Open-source Object-Relational DBMS
    - python-psycopg2 - PostgreSQL database adapter for Python
    - python-pip - Package management system used to install and manage software packages written in Python

- From pip
    - sqlalchemy - Python SQL toolkit and Object Relational Mapper
    - Flask - A lightweight Python web framework
    - oauth2client - Python library for accessing resources protected by OAuth 2.0
    - psycopg2 - PostgreSQL database adapter for Python

## Summary of configurations made:
- A new user was created with the name `grader` and password `gRad$1116#`. This user was given sudo access.
- Currently installed packages were updated with `sudo apt-get update && sudo apt-get install`
- Default ssh was changed to 2200, root ssh and password auth was disabled, and rsa authentication was enforced.
- Local timezone was configured to UTC with `sudo timedatectl set-timezone UTC`
- Uncomplicated Firewall(UFW) was set to only allow incoming SSH(2200), HTTP(80) and NTP(123) connections.
- Apache2 server was setup to serve a WSGI application.
- Postgresql was setup with a 'catalog' user with limited permissions

## Additional 3rd party resources used:
- [Using Flask with WSGI](http://flask.pocoo.org/docs/0.11/deploying/mod_wsgi/)
- [Postgresql Documentation](https://www.postgresql.org/docs/9.6/static/index.html)