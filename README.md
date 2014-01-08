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
