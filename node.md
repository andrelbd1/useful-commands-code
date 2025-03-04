### [Node](https://nodejs.org/en/)

### Install
- Install Node
````bash
    sudo apt install nodejs
````
- Install NPM
````bash
    sudo apt install npm
````
- Verify version
````bash
    nodejs -v
````
- Install NVM
````bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh
    source ~/.bashrc
````
- Check all available node versions
````bash
    nvm list-remote
````
- To install a node version
````bash
    nvm install v13.6.0
````
- Check node versions installed
````bash
    nvm list
````
- Alter node version to be used among the installed
````bash
    nvm use v13.6.0
````

#### General
- Create a project using react
````bash
    npx create-react-app [app name]
````
- Install node_modules
````bash
    npm install
````
- Run a project
````bash
    npm start
````
