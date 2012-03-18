### ``.rvmrc`` configuration to working with django projects.

This is a intent for easily working with django projects and never worry about trivial tasks like 
installing requirements and activate virtual enviroment for team members

####Basic workflow/usage:

project tree is like:

    -- project
       -- django-project
         -- manage.py
         -- requirements.txt
         -- dev-requirement.txt
         -- ...
       -- ...

Just put this ``.rvmrc`` file in your project root and rvm will do the magic.

Also you need to put ``requirements.txt`` and ``dev-requirements.txt`` inside your ``django-project``.

**requirements.txt** : file containing all requirements needed.

**dev-requirements.txt** : file containing all requirements needed for development like testing tools or something.

The first time you enter to your project, rvm will install requirements and dev-requirements and will generate a 
``d__.pyc`` and ``r__.pyc`` file inside your ``django-project`` to help it track the last time  requirements were installed; 
everytime you make a modification to any of requirements file, rvm will install the new requiremnts.


Optionally if you are using **git** you can put something like this in your ``.gitignore``:
    
    # Python
    *.pyc
    
    # Virtualenv
    /bin
    /include
    /build
    /lib
    /lib64
    /src
    /man
    /share
    .Python

**Note:** You need to have installed rvm http://beginrescueend.com/rvm/