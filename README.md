# Project 6 Linux Server Configuration
Configure Ubuntu server to host Item Catalog Web App.

## IP Address and SSH Port
IP address: **34.213.157.150**
SSH port: **2200**

## Complete URL to Web Application
**http://34.213.157.150**

## Configuration Summary
Set up server on Lightsail Ubuntu instance. Changed firewall settings to allow incoming connections from only SSH, NTP, and HTTP. Changed default port for SSH.

Created new user called **grader**. Gave sudo privileges to **grader** and created SSH key pair (Note: User **grader** requires password authentication for sudo tasks. Password will be provided in comments to reviewer.).

Disabled remote login for root user. Configured psql database with user **catalog** with limited privileges. Disabled remote connections for psql database. Configured Item Catalog Web App with psql and added domain to allowed domains list to Google Oauth. Had to use **xip.io** for url, as Google Oauth refuses to take IP address without some sort of '.com' ending. So registered domain looks like:
**http://34.213.157.150.xip.io**.

## List of Third Party Resources
Used UFW for firewall settings. Apache, mod_wsgi and postgresql for web application configuration. Used xip.io to configure web address name for Google Oauth registered domain list.