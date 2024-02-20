# todo
todolist
1. first set up virtual environment for the django file
2. using the following command(
   #create virtual environment
python -m venv venv
   #Then activate that environment
venv\Scripts\activate
    #Then install Django in that environment
pip install django
    #Then create django project named mysite
django-admin startproject todo
    #then create app
django-admin startapp todoapp
)
the todo and todoapp are gonna have some inbuild files
todo contains manage.py , setting.py, urls.py etc
&
todoapp will contain
todo
│
├── todoapp
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── venv/
│
├── manage.py
└── requirements.txt
3. two very important file are
   a. settings.py which will hold the project_wide configuration. INCLUDES A LIST OF ALL APPS THAT PROJECT KNOWS ABOUT AS WELL AS THE SETTING THAT DESCRIBE THE DATABASE TO BE USED
   b. urls.py has a list of all the Urls that the server must need
I.  The two __init__.py files are there, as usual, just to define their containing folders as packages.
II. The migrations/ subfolder will hold information about changes to your future database.
III. The models.py file will define the data model for your app.
IV. The views.py file will handle the logic controlling the app display.

5.  then we need to configure the projects so that it knows about the app inside ------> todo---> todoapp--------> settings.py ---> Inside it go into the INSTALLED APPS AND ADD todo(the settings.py will also contain interesting variables like DATABASES **setup by default to use sqlite3database using python **
6.  variables that affect our app security are 
  A. SECRET_KEY (IMP WHEN WE WANT TO PUT OUR APP ON 
                 PUBLIC SERVER GENERATED NEW EVERYTIME 
                  FOR NEW PROJECT)
  B. DEBUG :- USEFUL WHILE DEVELOPING THE APP SET TO 
              FALSE (iNITIALLY TRUE)BEFORE WE GO OUT 
              IN BIGBAD WEB : 
               REVEALS TOO MUCH ABOUT WORKING CODE
now colse the setting.py file and modify the urls.py (of todo and NOT todoapp)and add new urlpattern in tthe urls.py of the todo folder by :
        @ from import django.urls import include, path
    and inside urls pattern add
        @ path("", include(todoapp.urls"))
7. the create a new urls.py under todo--->todoapp and add
   urlspatterns=[]
   #for time being let it be empty
8. NOW inside todo directory in command prompt run the cmd :     py manage.py runserver
    after it run the http link and ourdjango project site will be visible on the web press ctrl+c in the cmd prompt to exit if our project is setup properly
   see (refer to the image)
9. design the data    
    
