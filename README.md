# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:

Create django application

### STEP 2:

write your code in models.py and admin.py

### STEP 3:

End of the program

Write your own steps

## PROGRAM

### models.py

```python
from django.db import models
from django.contrib import admin

# Create your models here.

class Student(models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    department=models.CharField(max_length=30)


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','department')
```

### admin.py

```python
from django.contrib import admin
from .models import Student,StudentAdmin

admin.site.register(Student,StudentAdmin)
```

## OUTPUT

### serveroutput
![std](https://user-images.githubusercontent.com/120539398/232966094-411cb8a1-83cc-45e6-bce3-a782548bd137.png)

### clientoutput
![co](https://user-images.githubusercontent.com/120539398/232966777-c05f84ac-802b-4201-a4ca-a6b4878b5287.png)


## RESULT
Thus the code has been executed successfully.
