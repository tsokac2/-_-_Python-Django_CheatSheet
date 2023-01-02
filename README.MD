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

### _NOTE_: Make sure the late Python version is installed and pip3 is configured in Environment Variables