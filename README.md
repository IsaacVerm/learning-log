# learning-log

## Python virtual environment (09-03-2019)

Make sure to install Python 3 directly from the site and not using Homebrew because of Mojave clusterfuck.

`virtualenv -p python3 venv`

`source venv/bin/activate`

Run `python --version`. Should say Python 3.x.x now. Default Python version in Mac is Python 2 so virtual environment is activated.

Run `pip install -r requirements.txt` to install the required packages in the correct version for this project . Further info about working with pip and virtual environments in Python can be found [here](https://docs.python.org/3/tutorial/venv.html).

Install additional packages by running `pip install package` and then `pip freeze > requirements.txt` to add it to the list of packages used in the project.

## Django (09-03-2019)

[tutorial](https://docs.djangoproject.com/en/2.1/intro/tutorial01/)

Scaffold project: `django-admin startproject scarf`

Following command start from project and not root of repo: `cd scarf`

Run local server: `python manage.py runserver`

Create app: `python manage.py startapp app`

Create tables: `python manage.py migrate`

## Tricks (09-03-2019)

Get timezone with `sudo systemsetup -gettimezone`.

## Handling multiple SSH keys

Multiple keys available in `~/.ssh` but only one of those is loaded at one time.

To load another key:

* check available keys `ls id_rsa*`
* remove all previous keys `ssh-add -D`
* load new key `ssh-add KEY`