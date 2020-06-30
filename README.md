# ProjectManagerFsdApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.18.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

## Push project to Github
> cd project-manager-fsd-app
> git init
> git add .
> git remote add origin https://github.com/rahulishu/project-manager-fsd-app.git
> git commit -m "first commit"
> git push -u origin master


## Install angular material
npm install --save @angular/material@8.2.3 @angular/cdk@8.2.3 @angular/animations@8.2.13


## Add Theme
add below theme import to styles.css
`@import '@angular/material/prebuilt-themes/deeppurple-amber.css';`

## Add Material icons
add below styles in index.html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">

## --dry-run
use this flag to view what will be generated

## Changes to run tests without actually opening chrome browser
use this command in angular CLI "ng test --watch=false --browsers=ChromeHeadless"


## create models class
> ng generate class models/user
> ng generate class models/project
> ng generate class models/parenttask
> ng generate class models/task
> ng generate class models/viewtask

## create component
> ng generate component users
> ng generate component projects
> ng generate component tasks
> ng generate component viewtasks

## create service 
> ng component service services/user
> ng component service services/project
> ng component service services/task
> ng component service services/viewtask

## Build docker image
> cd project-manager-fsd-app
> ng build --prod
> docker build -t project-manager-fsd-app:latest .

## Run image
> docker run --name project-manager-fsd-app -d -p 4200:4200 project-manager-fsd-app:latest
> docker container ls

## check nginx container if app is deployed 
> docker container exec -it <container_id> /bin/sh
> cd /usr/share/nginx/local
> ls 
> less index.html

## Push local image to docker hub registry
> docker tag project-manager-fsd-app:latest rahulishu/project-manager-fsd-app:latest
> docker push rahulishu/project-manager-fsd-app:latest

## Automated test result in testing document
Testing.docx

## CI/CD : Jenkins File to build and create docker image
create new item in Jenkins http://localhost:8080/
and add the jenkinsfile from git repository
