README
======

This is a basic example buildout for Pyramid

Installation
------------

Tested on Debian 7 [Wheezy] with python2.6 and python2.7

Make sure you have all dependencies you need, I prefer to install it into its own virtual environment::

        apt-get install build-essential python-virtualenv

go to/create /path/where/you/want/to/install/it for example /home/$USER/pyramid and create your vritualenv::

        virtualenv --python=python2.7 --no-site-packages $MYPROJECTNAME


**If you want to use python2.6, make sure you have installed all dependencies and replace python2.6 with python2.7**

after the creation its done do::

        cd $MYPROJECTNAME
        source bin/activate


Pyramid is installed using the buildout system. Installation is as straight forward as possible::

        git clone git://github.com/svx/pyramid-buildout.git buildout
        cd buildout

and now just do::

       python bootstrap.py
       bin/buildout

this will install Pyramid ...

Create your application::

        bin/pcreate -s starter MyProject

Installing your Newly Created Project for Development::

        cd MyProject
        python setup.py develop


Running The Tests For Your Application::

        python setup.py test -q



Running The Project Application::

        ../bin/pserve development.ini


Credits
-------
The Pyramid Framework http://www.pylonsproject.org//projects/pyramid/about





