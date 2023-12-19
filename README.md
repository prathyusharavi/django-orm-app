# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
start the program
### STEP 2:
get the  correct values from the program
### STEP 3:
end the  program


## PROGRAM
models.py

from django.db import models
from django.contrib import admin


#create your models here
class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    phoneno=models.IntegerField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','phoneno')

admin.py

from django.contrib import admin
from .models import Student,StudentAdmin
#register models here :
admin.site.register(Student,StudentAdmin)



## OUTPUT

![image](https://github.com/prathyusharavi/django-orm-app/assets/147474424/38e0c0c0-0749-4619-9332-407fdc5bd8c0)



## RESULT
thus the program successfully  created
