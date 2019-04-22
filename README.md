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

## Handling multiple SSH keys (17-03-2019)

Multiple keys available in `~/.ssh` but only one of those is loaded at one time.

To load another key:

- check available keys `ls id_rsa*`
- remove all previous keys `ssh-add -D`
- load new key `ssh-add KEY`

## Multiple instances of Visual Code in multiple windows

`code -n` from [StackOverflow](https://stackoverflow.com/questions/29964825/how-does-one-open-multiple-instances-of-visual-studio-code).

## Javascript fundamentals (22-04-2019)

Based on [Mozillla documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript).

### What is Javascript?

- interpreted
- first-class functions
- prototype based

Prototype based: creation of an object without first defining its class.

Functions first-class citizens:

- passing functions as arguments to other functions
- assign functions as variables

### Objects

#### [Basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)

An object is a collection of related data and/or functionality (which usually consists of several variables and functions — which are called properties and methods when they are inside objects.)

Dot notation does the same as bracket notation.

The this keyword refers to the current object the code is being written inside.

#### [OOP](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object-oriented_JS)

OOP = Object Oriented Programming

encapsulation = storing into object with a name (namespace)

Abstraction = creating a simple model of a more complex thing, which represents its most important aspects in a way that is easy to work with for our program's purposes.

Instantiation = When an object instance is created from a class, the class's constructor function is run to create it. This process of creating an object instance from a class is called instantiation — the object instance is instantiated from the class.

Inheritance = child classes inherit from parent class

Polymorphism = the ability of multiple object types to implement the same functionality

Constructor function = used to initialize object.

The constructor function is JavaScript's version of a class. You'll notice that it has all the features you'd expect in a function, although it doesn't return anything or explicitly create an object — it basically just defines properties and method.

Create new objects:

* object literal
* constructor function
* Object()
* create()

With create() you can create a new object based on any existing object

#### [Prototypes](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes)

Prototypes are the mechanism by which JavaScript objects inherit features from one another.

There are two types of inheriting:

* using prototype.call()
* ECMAScript 2015 class

Have to use super() to inherit when using class instead of call(). You also have to use getters and setters if you want to get/set properties.

Ultimately, objects are just another form of code reuse, like functions or loops, with their own specific roles and advantages.

It is a waste of time to use objects and inheritance just for the sake of it when you don't need them.

### JSON

JavaScript Object Notation (JSON) is a standard text-based format for representing structured data based on JavaScript object syntax.

Even though it closely resembles JavaScript object literal syntax, it can be used independently from JavaScript.

JSON exists as a string. It needs to be converted to a native JavaScript object when you want to access the data.

an array is also valid JSON.

JSON is purely a data format — it contains only properties, no methods.

Asynchronous JavaScript And XML (AJAX) is a programming practice of building more complex, dynamic webpages using a technology known as XMLHttpRequest.

The Fetch API provides an interface for fetching resources (including across the network). It will seem familiar to anyone who has used XMLHttpRequest, but the new API provides a more powerful and flexible feature set.


### [Javascript vs Java](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Introduction)

* no type checking
* follows most Java syntax
* no declaration of variables, ...
* no need to implement interface
* no need to worry about public/private methods
* prototype bases instead of class based

 The prototype-based model provides dynamic inheritance; that is, what is inherited can vary for individual objects.

 ### [Grammar and types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types)

 Variable scope: when you declare a variable outside of any function, it is called a global variable, because it is available to any other code in the current document. When you declare a variable within a function, it is called a local variable, because it is available only within that function.

 Hoisting: you can refer to a variable declared later, without getting an exception.

 Types of variables:

* var (global)
* let (block scope but can be reassigned)
* const (block scope but cannot be reassigned)

Data types:

* 

## Open questions

- how to install Javascript packages for a single project only using `yarn`?
