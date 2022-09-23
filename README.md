# Python-full-code 
# Operations 

from cmath import pi


print(10+20);
print(10-5);
print(10*5);
print(10/2); 
# Variables 
a = 5;
print(a); 
b = a+a;
c = a-a;
d = a*a;
e = a/a;
print(b,c,d,e); 
f = a*d 
print(f) 
# String 
a = 'hello world' 
print(a) 
b = len('hello world')
print(b) 
print(a[1]) 
print(a[6]) 
print(a[:2]); 
print(a[3:]); 
print(a[:-1]); 
print(a[-1:]); 
print(a[::2]); 
print(a[2::]); 
# String property 
b = a + ' welcome ';
print(b); 
c = 'manav' 
d = 'Hello ' + c;
print(d)  
a = 'M'
print(a*5); 
A = "Manav Sharma"
B = "How are you"
print(A.upper());
print(A.lower()); 
print(A.split()); 
print('Hello {}'.format(A)); 
print(" Hi {0} {1}".format(A,B))
print('Hi {p}'.format(p='manav'));
print("Thank you");

# List 
mylist = [1,2,3,4,5] 
print(mylist);
print(len(mylist))
print(mylist[1:])
print(mylist[:3]) 
for list in  mylist:
 print(list);
mylist2 = mylist *2 ;
print(mylist2)
mylist.append(6)
print(mylist)
mylist.pop(3)
print(mylist)
mylist3 = [8,3,4,9,1,5]
mylist3.sort() 
print(mylist3)
mylist.reverse()
print(mylist) 
mylist4 = [1,2,3,4,[1,2,3]]
print(mylist4)
print(mylist4[4][1]) 
for list in mylist3:
    print(list);
mylist5 = [[1,2,3],[4,5,6],[7,8,9]]
list = [row[1] for row in mylist5]
print(list) 
print(mylist5[1]) 
for list in mylist5:
    print(list)
# Dictionries 
Identity = {'Name':'Manav','Age': '22'} 
print(Identity['Name'])
print(Identity['Age'])
print(Identity.keys())  
# Tuple 
t = (1,2,3)
print(t)
print(len(t))
print(t.index(2)) 
print(t.count(2))
# Set 
x= set()
x.add(1)
x.add(2)
x.add(3)
print(x)
y = [1,1,2,2,3,4,5,6,6,7,8,9]
z = set(y)
print(z) 
# Boolean
a = 2 
b = 5 
c = None
print(a>b)
print(b>a)
print(c)
# Control Flow 
# Comparison  Operator 
a = 3 
b = 5 
print(a>b)
print(a<b)
print(a==b)
print(a!=b) 
# Logical Operator 
print(a>b and a<b) 
print(a>b or a<b)  
# Conditional Statements 
# 1. If statement 
x = 5 
if(x>1 and x<10):
    print("X in  range") 
# 2. If-else statement 
age = 24 
if(age>= 18):
    print("Eligible for vote")
else:
    print("Not eligible") 
# 3. If-elif statement 
age = 25 
if(age<=10):
    print("Child")
elif(age>10 and age<=18): 
    print("Adult")
elif(age>18 and age<=45):
    print("Man")
else:
    print("No age")
# Loops 
# 1. For loop 
a = [1,2,3,4,5,6]
for b in a:
    print(b)
for b in a:
    print(b+b)
for b in a:
   print(b*b)
for b in a:
    print(b-b)  
for b in a:
    print(b/b)
# for loop in dictonaries 
ages = {'Manav':22,'Pranav':17}
for keys in ages:
    print(keys)
for keys in ages:
    print(ages[keys])
# for loop in tuple 
mypair = [(1,2),(3,4),(5,6)]
for tub in mypair:
    print(tub)
for tub1,tub2 in mypair:
    print(tub1)
    print(tub2) 
#Range  
for i in range(5):
    print(i)
for i in range(1,10):
    print(i) 
for i in range(1,10,3):
    print(i)  
# List compreh3nsion
x = [1,2,3,4,5] 
print([item**2 for item in x])
# 2 . While loop 
i = 1 
while i<=10:
    print("Number is: {}".format(i))
    i = i+1 
# Function 
def add(num1,num2):
    return num1+num2; 

print(add(5,6)) 

def multi(num1,num2=5):
    print(num1*num2)
    return num1*num2 

multi(2)
print(multi(3)) 

def addOnlyeven(num1,num2):
    if(num1%2==0) and (num2%2==0):
        return num1+num2 
    else:
        return "False" 

print(addOnlyeven(10,2))
print(addOnlyeven(10,1)) 
# Object Oriented Programming (OOPs in Python)
class Person: #class
  def __init__(self, name, age): #constructor
    self.name = name
    self.age = age

p1 = Person("John", 36) # object


print(p1.name)
print(p1.age)



class Dog:
    def __init__(self,breed):
        self.breed = breed 

sam = Dog("Labra")
tommy = Dog("Bull dog")

print(sam.breed)
print(tommy.breed)
        
class Circle:
    pi = 3.14
    def __init__(self,radius=2):
        self.radius = radius
    def area(self):
        return  self.radius * self.radius * Circle.pi 
    
    def setRadius(self,radius):
        self.radius=radius 

    def getRadius(self):
        return self.radius 

c = Circle() 

print("radius is",c.radius)
print("Area is :",c.area())
c.setRadius(3)
print("radius is :",c.getRadius())
print("Area is :",c.area()) 

# Inheritance 
class Animal:
    def __init__(self):
        print("Animal created")
    
    def name(self):
        print("Animal name: ") 
    
    def eating(self):
        print("eat: ")
class Lion(Animal):
    def __init__(self):
        Animal.__init__(self) # Animal class inherit property to Lion class
        print("Lion created") 

    def name1(self):
        print("Simba")

    def eat(self):
        print("Hyna")

simba = Lion()
simba.name()
simba.name1()
simba.eating()
simba.eat()

class Person: 
  def __init__(self, name, age): 
    self.name = name
    self.age = age
    
  def __str__(self):
    return "name is {} ".format(self.name)

  def __len__(self):
    return self.age

  def __del__(self):
    print("Person destroyed")

 
p1 = Person("John", 36) 

print(p1.name)
print(p1.age)
print(p1)
print(len(p1))
del p1

