# Ex02 Django ORM Web Application
## Date:23/11/2026

## AIM
To develop a Django application to store and retrieve data from a Car Inventory Database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
```

admin.py

from django.contrib import admin

from .models import Car, CarAdmin

admin.site.register(Car, CarAdmin)

models.py

  from django.db import models
  
  from django.contrib import admin

  class Car(models.Model):
  
     car_id = models.CharField(
         max_length=20,
         primary_key=True,
         help_text="Car ID"
     )

     brand = models.CharField(max_length=100)
     model = models.CharField(max_length=100)
     year = models.IntegerField()
     price = models.IntegerField()
     fuel_type = models.CharField(max_length=50)
     quantity = models.IntegerField()
     color = models.CharField(max_length=50)

     def _str_(self):
         return self.brand + " " + self.model


 class CarAdmin(admin.ModelAdmin):
 
     list_display = (
         'car_id',
         'brand',
         'model',
         'year',
         'price',
         'fuel_type',
         'quantity',
         'color'
     )
```

## OUTPUT
<img width="973" height="600" alt="Screenshot 2026-11-22 101945" src="https://github.com/user-attachments/assets/7b2fbeab-05ff-4a84-ad27-dcee051b8d38" />
<img width="1916" height="1022" alt="Screenshot 2026-11-22 104753" src="https://github.com/user-attachments/assets/a390621a-ef4b-42d9-991d-c196465fc13e" />

## RESULT
Thus the program for creating car inventory database database using ORM hass been executed successfully
