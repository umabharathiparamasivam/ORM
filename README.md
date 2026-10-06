# Ex02 Django ORM Web Application
## Date: 06/10/2026

## AIM
To develop a Django Application to store and retrieve data from a Vehicle Service Database platform using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM
models.py
```
from django.db import models
from django.contrib import admin
class Vehicle_DB(models.Model):
    Brand=models.CharField(max_length=100)
    Manufacturing_Year=models.IntegerField()
    Colour=models.CharField(max_length=50)
    Vehicle_ID=models.IntegerField()
    Vehicle_No=models.CharField(max_length=10,primary_key=True)
    Phone_No=models.IntegerField()
    Owner_Name=models.CharField(max_length=50)
class Vehicle_DBAdmin(admin.ModelAdmin):
    list_display=["Brand","Manufacturing_Year","Colour","Vehicle_ID","Vehicle_No","Phone_No","Owner_Name"]
```
admin.py
```
from django.contrib import admin
from .models import Vehicle_DB,Vehicle_DBAdmin
admin.site.register(Vehicle_DB,Vehicle_DBAdmin)
```    


## OUTPUT
![alt text](<Screenshot 2026-10-06 222843-1.png>)


## RESULT
Thus the program for creating Online Food Delivery Database using ORM hass been executed successfully