virtual environment name : django_learning


DESIGN MAP :-

Create a cloud-based platform for teachers to upload and schedule - notes, flowcharts, diagrams, videos, presentations,
and others. Educators should be allowed to plan, organize, and display the curriculum for upcoming weeks for increased 
transparency.

Identify and execute apps that allow different users, such as—students, parents, and teachers—to post questions, 
reply to comments, and tag relevant subjects and users.


-Class
--subject 
---daily schedule 
---- notes, video, animation, ppt etc (study material)
------comments and replies (by anyone )

	
required apps: courses and users 

class models: 
- courses: class, subject, lesson, comments
- users: custom user model 

USERS: teachers, student, parents 


users model:  
- name (one to one with django user model)
- bio
- profile pic
- user_type 
** different user types will have different accessibility


class model: 
- name of class (10, 11 etc.) (id)
- description 

subject 
model: 					
- subject_id (id)
- subject name 			
- class (foreign key)	
- image 		
- description 

lesson model: 
- lesson_id (id)
- standard (foreign key)
- created by (user - foreign key)
- created at
- subject (foreign key)
- lesson_name 
- position (chapter no.)
- video
- ppt
- notes

Comment model:
- lesson name (foreign key)
- comm_name 
- author (user -foreign key)
- body 
- date_added (datetime)


reply model:
- comment_name (foreign key)
- reply_body 
- author (user -foreign key)
- date_added (datetime)

 



FLOW OF DJANGO APP :-
- create a virtual environment 
- install django
- django-admin startproject <project name>
- django admin startapp <app name>
- 	add the app to settings.py in installed apps
- 	add views in app from views.py
- 	map this view to urls.py (using url mapping or include function)
- add templates
- 	add templates folder and add subdirectories of each app  
- 	change the directory to get these templates in project settings (DIR): 
	adding the templates dir to the django project to fetch html files: TEMPLATE_DIR 
- 	adding this in templateslist in settings.py 
- 	create html file inside the templates directory and put html code
- Edit views.py to take the template
- make all the models 
- 	python manage.py migrate
- 	register the changes in model: python manage.py makemigrations <app name>
- 	python manage.py migrate
- 	register your models in admin.py file of that application
- 	create superuser to get access to admin interface
- create a forms.py to use the models in front end for users (django-crispy-forms for bootstrap support)
- create templates for registration, login, base, index html files in respective subdirectory of templates folder
	create a base.html and use template tagging to extend this on all other pages
- a to and forth between forms, html and views files to setup what we want. 

PYHTON MANAGE.PY RUNSERVER	
- 
- 



open python anywhere 
go to console and type "mkvirtualenv --python=python3.7 teaching_blog(env name)"
install dependencies 
which django-admin.py to check if the django is successfully installed and working
git clone <repo name>
get dir list using ls and get into file 
migrate and make migrations like we do locally
create superuser
go to web, add project 
add virtual env on path (/home/somvirs57/.virtualenvs/teaching_blog)
open bash console in virtual env and get the working directory by getting 
		into the directory and typing pwd
paste this path into source code directory

setup wsgi.py file - delete hello world
		   - go to django 
		- uncomment import os,
		- change path to your working path
		-add os.chdir(path)
		-settings environment to your settings file

add site to allowed host in settings
		
add static files - staic , media and admin/static


- 
- 
- 
- 