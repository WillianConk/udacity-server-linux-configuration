# Udacity server linux configuration

## How to Access the server

- Application is running at http://100.26.248.95/ in port 80.
- Server is ubuntu, Running on amazon lightsail

## What is under the hood

- The server is running the following application (https://github.com/WillianConk/catalog)
- The application is being served from apache2, with python-wsgi
- Application runs on python 2.7 with flask
- Database is a simple sqlite
- Firewall is UFW 

## How did I configure this server

- First I installed UFW, and closed all the ports, except the ones required by Udacity;
- Then I created an user called grader, enabled sudo access, and enabled his SSH access;
- Edited SSH configurations to disallow root access, and password access, restarted ssh;
- Installed apache2, and the required modules for python-wsgi;
- Installed python2, pip, and the application dependencies;
- cloned https://github.com/WillianConk/catalog;
- Configured apache to serve the application;
- Set the folder permissions at /var/www/catalog to enable apache to read the sqlite db file;
- profit 🚀
