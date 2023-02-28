# Topic: Project Setup / Setting Up The Development Environment:

## Essentials:
- python --version
- pip install pipenv   
<!-- Pipenv package manager, for managing dependencies in Python projects through pipfiles  -->

## Project Setup / Setting Up:
- mkdir directoryname
- pipenv install django
- pipenv shell 
<!-- For activate virtualenv -->
- django-admin startproject myproject .
<!-- last . for in current working directory -->
- python manage.py runserver  
   ### Using Integration Terminal in VSCode:
   - pipenv --venv
     <!-- This is for activating venv in terminal automatically -->
     <!-- type in cmd provide venv path|past it in interprater path with /bin/python-->
 
# Create app:
- python manage.py startapp appname
  <!-- add app name in settings.py apps section  -->

# Templates:

1. Create template in first app
   <!-- - If you do this, you dont need to play settings.py to add the template -->
2. Create in outside 
   <!-- - Then you need to add the template to the settings.py template section
        - also need to add the static file path in settings.py -->

### Change Template Through view.py:
  @view.py
- return render(request, "index.html", {"name": "Ahmad"})      
  <!-- pass dictionary to add value in template -->
  @.html
- hello {{name}}
  <!-- for putting value here -->

### Add python condition in template:
  - {%if name%}
    <h1>hello {{name}}</h1>
    {%else%}
    <h1>hello world</h1>
    {%endif%}
    <h1>hi,</h1>  
