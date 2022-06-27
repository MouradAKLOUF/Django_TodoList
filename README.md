# Django_TodoList
  
Web Application to make ToDo list for each user built with Django and sqlite  
features: register/login/logout users  
          add todolists of each users  
          add items for each todolist/user  
  
# Django cheat sheet  
  
# prepare env  
python -m venv <env name>   
<env name>\Scripts\activate    
pip install django    
pip install django-crispy-forms     
pip install requuirements.txt    
deactivate    

#start app  
django-admin startproject <project name>  
python manage.py runserver 5050  
python manage.py startapp <app name>  
  
python manage.py makemigrations <app name>  
python manage.py migrate  
<-- you may want to remove migration files + old database -->  

# manips database from python shell  
python manage.py shell  

from main.models import Item, ToDoList   
list1 = ToDoList(name="mourad todolist 01")     
list1.save()   
print(list1.id)   
print(ToDoList.objects.all())  
find_list = ToDoList.objects.get(name="Tim's list")  
print(list1.item_set.all())  
list1.item_set.create(text="Go to the mall", complete=False)    
list1.name = "new name"  
list1.save()   
list1.delete()   

# create admin account  
python manage.py createsuperuser  

