### [Python](https://www.python.org/) commands

#### Python General
- Checking python version
````bash
    python --version
````
- Remove all all .pyc and .pyo files as well as __pycache__ directories recursively starting from the current directory
````bash
    find . | grep -E "(/__pycache__$|\.pyc$|\.pyo$)" | xargs rm -rf
````
- Understand how a particular function or module works
````bash
    help(<FUNCTION or MODULE>)
````

#### Virtualenv General
- Create virtual env and install libs from requirements file
````bash
    virtualenv venv
    source venv/bin/activate
    pip install -r requirements.txt
````
- Update virtual env from requirements file
````bash
    pip install -r requirements.txt --upgrade
````
- Setting a python version
````bash
    sudo add-apt-repository ppa:deadsnakes/ppa
    sudo apt install python3.10 python 3.10-distutils
    curl -sS https://bootstrap.pypa.io/get-pip.py | python3.10
    
    virtualenv -p /usr/bin/python3.10 venv
````

#### Pyenv General
- Download pyenv
````bash
    curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
````
- Set .bashrc
````bash
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
    echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
    echo 'eval "$(pyenv init -)"' >> ~/.bashrc
    source ~/.bashrc
````
- Update list of python version
````bash
    pyenv update
````
- Install python by version
````bash
    pyenv install 3.11.5
````
- Uninstall python by version
````bash
    pyenv uninstall 3.11.5
````
- Setting a python version
````bash
    pyenv shell 3.12.6
````
- Create virtual env and install libs from requirements file
````bash
    python -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt
````
- See python versions installed
````bash
    pyenv versions
````
- Search version available to install
````bash
    pyenv install --list | grep "3\.[678]"
````

#### PyTest
- Run cover test
````bash
    py.test --cov=src tests
````
- Run cover test and report to xml using sonnar
````bash
    py.test --cov=src --cov-report=xml tests
````
- Run a test
````bash
    py.test tests/src/controllers/test_<file-name>.py -k test_<file-name>
````

#### Flake8
- Run flake8
````bash
    flake8 [file or dir]
````

#### Sonnar
- Run Sonnar
````bash
    sonar-scanner -Dproject.settings=sonar-project-local.properties
````

#### Snyk
- Run Snyk
````bash
    snyk test
````
