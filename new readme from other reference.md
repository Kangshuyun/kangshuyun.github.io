CREATE todoapp---> todo--->add todo to settings.py and create view for the htmlfile and 
        |                  add this view to urls.py of todo(only make changes at the bottom)
        |                  now go to settings.py and makechanges to the template list and find 
        |                  section called DIRS AND now create a model todo_list_item(to represent each todo item 
        |                  the model will automaticalley create and store the item in the database
        |                  open cmd prompt and type (python manage.py migrations)
        |                  after execution next cmd: python manage.py migrate (by this we will be able
        |                   able to view the changes)
        |                  retrieve todo-items to the view.py file
        |                  open view.py and import the model todo_list_item
        |                  create new variable to store the todoitems and return it to template list
        |                  
        |
        |
        |------> templates ---> todohtml.html


1. INSTALL DJANGO (pip install django) NOTE: on linux or mac os pip3 install django
2. Start a new project (django-admin startproject projectname(ours is todoapp))
3. all the files will be set up in folder called todoapp like ( + extra todoapp file inside
   + __init__ + settings.py + urls.py + wsgi.py + manage.py)
4. now get inside the create project(cd todoapp)
5. after getting into the folder run command: python manage.py runserver
6. open the url displayed on the cmd prompt by copying and pasting on any webbrowser
7. NOW create an app inside the todoapp and lets name it todo for now :
    python manage.app startapp todoapp
                OR
    django-admin startapp appname(ours is todo)
8. now get inside the todoapp directory open settings.py and in INSTALLED APP ADD THE APPNAME
   WE JUST CREATED WITH SINGLE INVERTED COMMA
9. cREATE A TEMPLATE INSIDE THE TODOAPP CMD (mkdir templates)
10. and inside  'TEMPLATES 'this we are gonna create and html file cmd :
           cmd :
11. now the html file will be created and lets give heading and tittle to our html file
12. NOW GO TO VIEW.PY( INSIDE TODOAPP) AND ADD THE view for template
13. from django.shortcuts import render
    def todoappView(request):
    return render(request, 'todohtml.html')        #todohtml.html is our html filename
14. NOW WE NEED TO LINK THE VIEW TO THE URL 
