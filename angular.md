### [Angular](http://angular.io) commands


#### Project
- Create a project
````bash
ng new name-project
````
- Open a project
````bash
cd name-project
ng serve --open
````

#### Component
- Create a component
````bash
ng generate component name-component
````

#### Service
- Create a service
````bash
ng generate service name-service
````

#### Module
- Create a module
````bash
ng generate module name-module
````
- Put the file in `src/app` instead of its own folder
````bash
ng generate module name-module --flat
````
- Tells the CLI to register it in the imports array of the AppModule
````bash
ng generate module name-module --module=app
````
