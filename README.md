# django-todo
A simple todo app built with django

### Setup
To get this repository, run the following command inside your git enabled terminal
```bash
$ git clone https://github.com/rohandinda/django-assingment.git
```
Generate an Access token on your GitHub.
After then install jenkins and get it running on your EC2 (make sure to open port 8080).

Integrate jenkins and github:-
manage jenkins> manage plugins> select git client

Give jenkins personal access token:-
configure system> GitHub> AddGitHub server> Add credentials> kind(secret text)> set the access token of your GitHub.

Making CI/CD Pipeline:-
1)create a job.
2)source code management> Git> give repo url.
3)give the name of branch.
4)Build Step> Execute shell:-
  sudo docker build . -t todo-app
  sudo docker run -p 8000:8000 -d todo-app
5)Build Now



