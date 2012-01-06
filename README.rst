README
======

This is a basic example buildout for Pyramid

Installation
------------

Tested on Debian 7 [Wheezy] with python2.6 and python2.7

Make sure you have all dependencies you need/want, i prefer to install it into its own virtual environm
ent::

        apt-get install build-essential python-virtualenv

go to/create /path/where/you/want/to/install/it for example /home/$USER/pyramid and create your vritualen
v::

        virtualenv --python=python2.7 --no-site-packages $MYPROJECTNAME


*If you want to use python2.6, make sure you have installed all dependencies and replace python2.6 with python2.7* 

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

        mkdir src && cd src/
        ../bin/paster create -t pyramid_starter myproject

Adopt your buildout and add src/myproject to develop-eggs and myproject to eggs parameter in [pyramid] section [see comments in buildout.cfg]

Rerun buildout and start your application::

        ./bin/buildout -Nvvv
        ./bin/paster serve src/myproject/development.ini

Credits
-------
The Pyramid Framework http://www.pylonsproject.org//projects/pyramid/about
Simon Pamies http://simon.pamies.de

        




