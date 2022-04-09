# angular-project-template
This is a template for future angular projects.
It is all stuff that I tend to forget and I need to google everytime I start a new project. Feel free to copy it and ask questions.

For now it is purely Angular, but I will probably add more parts as I go on.


# Replicate the project
```
ng new application-name
cd application-name
npm install bootstrap
```
Add the following to `application-name/styles.sass`
```
$purple: #9926f0
$primary: $purple

@import "../node_modules/bootstrap/scss/bootstrap"
```
## Docker
```
docker build -t angular-template:20220409
docker run -d -p 8080:80 angular-template:20220409
```