Rank-me bootstrapper
====================

This bootstrapper allows you to install Rank-me very easily on a Debian server.

How to use it
-------------

First, install ansible (you can do that in a virtual environment):

    pip install ansible

Next, edit the `hosts.ini` file and adapt it to your needs (make sure you set
the `SECRET_KEY` variable).

Finally, run the following command:

    ansible-playbook -i hosts.ini playbook.yml

You should then be able to access the rankme instance on the URL you provided
in the `hosts.ini` file (variable `server_name`).

Creating a superuser
--------------------

This install process doesn't create a superuser, so if you want one you'll have
to create one by yourself. To do so, just SSH to your server and run (replace
`/var/www/rankme` by your own `install_path`):

    /var/www/rankme/ENV/bin/python /var/www/rankme/rankme/manage.py createsuperuser
