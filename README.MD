<h1 align="center">Get Started - Python and Django</h1>

## Set up Python on Visual Studio Code

* In the command line check the Python version:
```python --version```

* If Python is not installed, download the installation file from **[HERE](https://www.python.org/downloads/)**

#### Configure  PATH **Environment Variables** in Win 10 for ```pip3``` python installer program

* Open Environment Variables - **Start** - type **"Path"** - click on **Edit the System Environment Variables**
* Under **User variables for <user>** - **New** - Create a name for pip3 variable - copy/paste ```pip3.exe``` file location in the **Variable value** field.
* Under **System variables** - Select **Path** - **Edit** - copy/past file location - ex. ```C:\Program Files\Python311\Scripts```
* In the comand line test with ```pip3``` comand.
* Result for a successful configuration
```
Commands:
  install                     Install packages.
  download                    Download packages.
  uninstall                   Uninstall packages.
  freeze                      Output installed packages in requirements format.
  inspect                     Inspect the python environment.
  list                        List installed packages.

Show help for commands.
...
```
* Update Python Version **[Upgrade Python](https://monovm.com/blog/how-to-update-python-version/)**

* In Visual Studio Code create a Python file with ```*.py``` extension

* In Visual Studio Code install the extension by pressing **Ctrl+Shift+X** and installing the 2 extensions

    ``` Python - ms-python.python```

    ``` Code Runner```

* In  Visual Studio Code under **"Settings"** find the **"Text Editor - Code Actions On Save"** open ```settings.json``` and _copy/paste_ the following line:
```"code-runner.runInTerminal": true,```

* Run the Python files in the command line by typing the following:

    ```py PATH/file.py```

    or
    
    ``` python PATH/file.py```
    
    or
    
    Press the **"Play"** button in the _top-right corner._

## Start Django Project

### _NOTE_: Make sure the [latest Python](https://www.python.org/downloads/) version is installed and pip3 is configured in Environment Variables

* Create project folder: 

    ```mkdir <Project Folder>```

* Navigate in the project folder and create a Django project:

    ```pipenv install django```

```
Successfully created virtual environment!
Virtualenv location: C:\Users\Tomislav\.virtualenvs\django-LQQolwqZ
Creating a Pipfile for this project...
Installing django...
Pipfile.lock not found, creating...
Locking [packages] dependencies...
Locking [dev-packages] dependencies...
Updated Pipfile.lock (af42abefb766e975f7680f10368735353569fb4fe0114e59496a7202658362fc)!
Installing dependencies from Pipfile.lock (8362fc)...
To activate this project's virtualenv, run pipenv shell.
Alternatively, run a command inside the virtualenv with pipenv run.
```
* Use the following to open VS Code from the terminal ``` code . ```
* Activate Virtual Environment with 

    ``` pipenv shell```

* Create Django App with 
    
    ``` django-admin startproject myApp .```
* Run Django server with 
    
    ```python manage.py runserver```

```
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.        
January 02, 2023 - 10:26:13
Django version 4.1.5, using settings 'myApp.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.
```
