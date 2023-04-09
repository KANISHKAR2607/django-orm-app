# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![lab02 ER](https://user-images.githubusercontent.com/118886772/230779471-a1bec577-228a-4cc7-bc89-d4ec5588fb10.png)

## DESIGN STEPS

### STEP 1:
Create a django application using django-admin startapp in command line. Head to the application directory created inside the project directory. Open the models.py file. In models.py create two classes one defining the attributes and the other one defining attribute value types.

### STEP 2:
In the same directory, Head to admins.py and import the two classes from models.py that you have created earlier. Now register your created models in admins.py file and save both the files

### STEP 3:
Start the Django server and head over to admin page. Using the admin interface, you can add or delete data in the data

## PROGRAM
```
from django.db import models
from django.contrib import admin
class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    gender=models.CharField(max_length=100)

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','gender')
    
```    
    

## OUTPUT
### SERVER OUTPUT

![lab02 server output](https://user-images.githubusercontent.com/118886772/230779345-da71aded-0686-4950-9c51-285730d1222f.png)
![Screenshot 2023-04-06 094431](https://user-images.githubusercontent.com/118886772/230779349-b39297ae-2d01-4c85-bff1-602e6d482b35.png)

### CLIENT OUTPUT

![lab02 client output](https://user-images.githubusercontent.com/118886772/230779383-6dd11000-f869-41d3-93b8-0876c76d4ca6.png)
![lab02 client output 2](https://user-images.githubusercontent.com/118886772/230779398-95e345ef-a2a0-4910-b1b4-45b772e585fd.png)

## RESULT
A Django application has been created that can be used to store and retrieve data from the database using Object Relational Mapping(ORM).
