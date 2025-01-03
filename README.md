# sttemplate
A minimal viable template repo for streamlit projects and publishing them on
PyPi  

The repo comes with everything you would need to get started making scalable,
maintainable python ackages.  
This summarizes alot of what I had to learn to develop and maintain [Streamlit Analytics2](https://github.com/444B/streamlit-analytics2)

>[!TIP]
> How to use this repo
> 1. make a [fork](https://github.com/444B/sttemplate/fork)
> 1. clone it to a workstation
> 1. start adding your code into the src/ folder
> 1. add your dependencies (I will add a guide to this if there is interest, just open an issue)
> 1. test it by writing unit test in the tests/ folder and running checks.sh
> 1. set up Github action CI/CD and deploy to Pypi!

Here is the layout and a description below for each section
  
├── [README.md](https://github.com/444B/sttemplate/blob/main/README.md#-readmemd)   
├── [pyproject.toml](https://github.com/444B/sttemplate/blob/main/README.md#-pyprojecttoml)  
├── [src](https://github.com/444B/sttemplate/blob/main/README.md#-src)  
│   └── [sttemplate](https://github.com/444B/sttemplate/blob/main/README.md#----sttemplate)  
│       ├── [__init__.py](https://github.com/444B/sttemplate/blob/main/README.md#--------initpy)  
│       └── [app.py](https://github.com/444B/sttemplate/blob/main/README.md#--------apppy)  
├── [tests](https://github.com/444B/sttemplate/blob/main/README.md#-tests)  
│   ├── [checks.sh](https://github.com/444B/sttemplate/blob/main/README.md#----checkssh)  
│   └── [test_calc.py](https://github.com/444B/sttemplate/blob/main/README.md#----test_calcpy)  
└── [uv.lock](https://github.com/444B/sttemplate/blob/main/README.md#-uvlock)  

---  
## ├── README.md

This is the document you are reading at this very moment. It is essential to 
sharing what your project is about and how to use it.  

--- 

## ├── pyproject.toml

This is a crucial part of your project and can be used for managing
dependancies, configurations, and if you deploy to PyPi then it is the info on
the sidepanels.  

--- 

## ├── src

This is the top level folder where your actual code will be.  

--- 

## │   └── sttemplate

This sub level folder is the name of your project and package and organizes your
code even further.  
You would have one of these for each module you write but you need at least 1.  

--- 

## │       ├── __init__.py

This very important file indicates to other python files that it organizes your
code into a module and can be imported with `import sttemplate`.  
Inside, you would define which functions and which files specifically are
availible  

--- 

## │       └── app.py

Here is where the magic happens. Your Million dollar idea, the next IYKYKaaS.
This is why you get paid the big bucks but as you might be observing that quite
alot goes on to make that magic code availible.  

--- 

## ├── tests

This folder is essential for observing the true scale of your application with
scale and complexity. `print()` and `logging.info` will only take you so far
Especially as you add features and make unpredictable changes, you will use code
here to test the `src/` code for correct behaviour.  
They also help our code be more readable and maintainable.  

--- 

## │   ├── checks.sh

This is a custom script I came up with that collects alot of python packages
used for testing:  
- black = formatting  
- isort = import sorting  
- flake8 = linting  
- mypy = type checking  
- bandit = basic security checks  
- pytest = unit testing  

--- 

## │   └── test_calc.py

This is just an example of a pytest file that demonstrates how to do a unit test
and also verifies that the imports set out in __init__.py work as intended.  

--- 

## └── uv.lock

This section is opinionated since it touches on the topic of dependancy
management. [UV](https://docs.astral.sh/uv/) is a tool for managing all these 
dependencies and in my opinion it does a fair job of it. 
There are many dependency managment tools such as pip, pipenv, poetry, tox or
even just rawdogging it with `python -m`. Try them out and find what works best for you

---
