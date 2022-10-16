# JApi 

An automated backend system. (back-end ☠️)

## 📓 About

JApi is a termianl app written using shell, python and django. It is an easy
way to create your own backend server where the code for the same can also be accessed.
It writes the code automatically depending on the json which is being provided by the 
user. It also provides the user with endpoints depending on the json which is being 
provided by the user. Django along with the Django Rest Framework are used the same. 
We can change the primary keys and can also describe connection between the databses, 
hence establishing a connection. The tables will be autogenerated and it's name and other
details and the table can be changed whenever needed. TUI is made using the package click, 
fascilitating work on the terminal. 
It's major outome and goal is to generate a backend easily and without wiriting much 
code, with ease. Moreover the code for the backend will also be accessible to the user. 
The user can then make changes to the code according to their requirements. This will 
be a helpful tool for developers who do not wish to re-write the same codes and can 
add other important feature like authentication etc to the basic code which is being 
generated using this terminal app. 

[![Youtube Video link of Notesy](http://img.youtube.com/vi/W4jO667ISF0/0.jpg)](http://www.youtube.com/watch?v=W4jO667ISF0 'JApi')
## 💡 Motivation


The idea of this project arose while thinking of how can we make it easier for a 
developer to write backend. For example, if a frontend developer wants to integrate 
backend to their project, they are left with only one option of learning how to 
code it. To make it easier for them, and giving in a basic layout of the 
backend, we came up with this idea to automate Django based on the json given by 
the user. Another usage of this is when an experienced developer wants to make an 
advanced project, they can use this and create a basic layout which they can later 
edit according to their convinience and can add more complex functionalities like 
authentication to the layout. This also saves the time which is wasted in 
re-writing codes. 


## 🚀 Features

<ul>
    <li> Create your own backend server, depending on the json which is provided by the user. </li>
    <li> Access the codes for the same and can ammend them as per need.  </li>
    <li> Provides the user with endpoints. </li>
    <li> Can change the primary keys and the tables </li>
    <li> TUI is made using the package click, fascilitating work on the terminal. </li>
    <li> Can establish connection between the tables which are auto-generated. </li>
    <li> Can access the basic code which is generated and can add other important features, hence saving time. </li>
</ul>

## 🤖 Tech Stack

Following tech stacks have been used to create this project <br>

- <b>React</b><br> Shell, Python, Django and its frameworks along with 
the package Click is used to build this terminal app. 
The algorithm behind the app and the code for establishing the connections 
between the table is written using Python. 

- <b>Shell </b><br> Shell is used in run a group of terminal commandas 
automatically using python code which is a pre-requisite. 

- <b>Django </b><br> Django along with Django Rest Framework are used to create 
the automated backend server. 

- <b>Python </b><br> The algorithm behind the app and the code for establishing 
the connections between the table is written using Python. The package Click is used for TUI. 

## 📦 Usage
### Prequisite

- virtual environment 
- [ubuntu](https://docs.python-guide.org/starting/install3/linux/)
- [python3](https://docs.python-guide.org/starting/install3/linux/)
- pip

Make sure that these things are already installed in you PC before using `jApi`.
Now clone this repository in a directory where you want to create your backend.

### Flags information

- `-i` or `--init` : This flag is used to initialize the backend generation with default names of project (`backend`) and app (`base`). This flag will generate your boiler backend and will start the server at port 8000. This flag has two options:
    - `-d` or `--directory` : This option will allow you to configure the name of the project.
    - `-s` or `--sub_directory` : This option will allow you to configure the name of the app.

- `-a` or `--append` : This flag is used to create a new schema/table. It has three options:
    - `-j` or `--json_path` : This option will allow to provide json file path. Is is a kind of mandatory option.
    - `-c` or `--class_name` : This will allow you to change the name of your table/schema.
    - `-pk` or `--primary_key` : This will allow you to assign an attribute of json as the primary key of that schema/model.

- `-con` or `--connect` : This flag is used to create a connection between two models. It can be use multiple times to create multiple connection between any models. It has three options, all of which are compulsory.
    - `-f` or `--from_database` : Here you will have to provide the class name of the schema `from` which you have to make the connection.
    - `-to` or `--to_database` : Here you will have to provide the class name of the schema `to` which you have to make the connection.
    - `-ct` or `--con_type` : Here you will have to provide the type of connection that you have to make between the schemas. It has only three inputs:
        - `o2o` : This will make a `one to one` connection between your schemas.
        - `o2m` : This will make a `one to many` connection between your schemas.
        - `m2m` : This will make a `many to many` connection between your schemas.
### Examples
- ```
    python3 main.py -i
    ```
    Initialises the django boiler project with project backend and app base<br>
- ```
    python3 main.py -i -d dir -s subdir
    ```
    Initialises the django boiler project with project dir and app subdir<br>
- ```
    python3 main.py -a -j test.json
    ```
    Creates a database with name test and primary key as id (automatically generated uuid.Uuid4)<br>
- ```
    python3 main.py -a -j test.json -c Dummy -pk username
    ```
    Creates a databse with name Dummy using the schema of test.json The primary key is set to username. username must be a key of test.json<br>
- ```
    python3 main.py -con -f Mod1 -to Mod2 -ct o2o
    ```
    Creates a one to one connection between Mod1 and Mod2 tables




## 🔨 Contribute

### Minimum system requirements to run this project

- Ubuntu
- Python 3
- Python 3 pip
- Python venv
- Internet Connection

### Procedure

- Fork and clone the repo to your local system. 
- Open a new terminal in the same folder
- Run this command<br>
    ```
    python3 main.py –i
    ```
- Your server should be running
- Open another terminal and add some models by providing json files using this command<br>
    ```
    python3 main.py -a -j test.json
    ```
- This will create a schema in the backend as specified in test.json files.
- You can make more schema by providing more json files and also try to create connection between them.

Now make the changes, propose a feature and make a PR.
