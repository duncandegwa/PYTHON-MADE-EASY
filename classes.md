### Creating and Using a Class
```py
class Ndegwa():
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def myname(self):
        print(self.name.title() + "is my name")
    def myage(self):
        print(self.age + " is my age")

me = Ndegwa('DUNCAN', '12')
print(me.myname())
print(me.myage())  
```

### Working with Classes and Instances
```py
class Car():
    def __init__(self,model,year,name):
        self.model=model
        self.year=year
        self.name=name
        self.speed=0  # Default Value
    def get_all_properties(self):
       all_p=self.name+self.model+str(self.year)
       return all_p.title()
mycar=Car('V12',2020,'VOLVO')
print(mycar.get_all_properties())
class Supercar(Car):
    def __init__(self,model,year,name):
        super().__init__(model,year,name)
        self.color='blue'

    def mycolor(self):
        print("MY COLOR IS" + self.color)
mytesla=Supercar('V12',2020,'SUZUKI')
mytesla.get_all_properties()
print(mytesla.get_all_properties())
print(mytesla.mycolor())
```