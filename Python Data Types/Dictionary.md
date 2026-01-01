# Dictionary( Dict)
Dictionaries store items in " keys : values " pairs
In versions Python 3.7 and newer , dict is sorted, while in 3.6 and older dict in unsorted
Dictionary is changeable data type, consisting of any of other data types
Duplicates don't exist , but allowed. They will overwrite already existing values
```py
dict1 = {
    "name": "Anvar", #string
    "age": 18, #integer
    "student": True, # boolean
    "subjects": ["CAL1", "P1","PE1","AE1","AER","OOP1","INTRO TO IT"], # list
    "age": 20 # integer
}
print(dict1)
```
You can also create dictionary with constructor dict()
```py
thisdict = dict(name = "John", age = 36, country = "Norway")
```
# 1. Access Items
```py
dict1 = {
    "name": "Anvar",
    "age": 18,
    "student": True
}
x = dict1["name"]
y = dict1.get("name")
z = dict1.keys()
w = dict1.values()
v = dict1.items()
```
1. Direct output
'x' will refer to value of 'name' key, not store it. So ,when you change it , value of 'x' will change too.
2. Get method
'y' will store value of 'name' key, not reger to it
3. Keys method
'z' will store list of keys ["name","age","student"]
4. Values method
'w' will store list of values ["Anvar",18,True]
5. Items method
'v' will store list of sub-lists of [('name','Anvar'),('age',18),('student',True)]
# 2. Add/Update Items
Update method ( if exist key, updates it. Else add new)
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})
thisdict.update({"color": "red"})
```
Direct change ( if exist key, changes it. Else add new)
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["year"] = 2018
thisdict["color"] = "red"
```
# 3. Remove Items
Method pop() through specified key
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model")
```
Method popitem() deletes last added key with its value 
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop()
```
'del' Method through specified key ( with [] braces )
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict["model"]
```
By the way, 'del' can also delete dict itself
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict # Deletes dict completely
```
Method clear() empties dict
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.clear()
```
# 4. Loop Function of Dictionaries
Print all keys by index and key() method
```py
for x in thisdict:
  print(x)

for x in thisdict.keys():
  print(x)
```
Print all values by index and values() method
```py
for x in thisdict:
  print(thisdict[x])

for x in thisdict.values():
  print(x)
```
Print both keys and values with items() method
```py
for x,y in thisdict.items():
  print(f"{x} : {y}")
```
# 5. Copy Dictionaries
You cannot copy a dictionary simply by typing dict2 = dict1, because: dict2 will only be a reference to dict1, and changes made in dict1 will automatically also be made in dict2
Instead there are : copy() method and constructor dict()
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict1 = thisdict.copy()
mydict2 = dict(thisdict)
```
# 6. Nested Dictionaries
```py
child1 = {
  "name" : "Emil",
  "year" : 2004
}
child2 = {
  "name" : "Tobias",
  "year" : 2007
}
child3 = {
  "name" : "Linus",
  "year" : 2011
}

myfamily = {
  "child1" : child1,
  "child2" : child2,
  "child3" : child3
}
```
This creates myfamily dict, that contains data of 3 children( child1, child2, child3 )

Getting Access to the specific data we can by method:
main_dict["name_of_nested_dict"][name_of_key]
```py
Name_Of_Child2 = myfamily["child2"]["name"]
```

Get all data of nested loops we can by nested for loop and items() method
```py
for name_of_nested_dict, keys_of_nested_dicts in myfamily.items():
    print(name_of_nested_dict)
    
    for y in keys_of_nested_dicts:
        print(y + ':', obj[y])
```
With items() method: name_of_nested_dict -> becomes keys of main dict(names of sub dicts),
keys_of_nested_dicts -> becomes values of main dict(keys of sub dicts),
y -> becomes values of sub dicts
```py
#Full version of Nested Dict above
myfamily = {
  "child1" : {  "name" : "Emil",  "year" : 2004},
  "child2" : {  "name" : "Tobias",  "year" : 2007},
  "child3" : {  "name" : "Linus",  "year" : 2011}
}
```
# 7. Methods
```txt
clear()           Removes all the elements from the dictionary
copy()            Returns a copy of the dictionary
fromkeys()        Returns a dictionary with the specified keys and value
get()             Returns the value of the specified key
items()           Returns a list containing a tuple for each key value pair
keys()            Returns a list containing the dictionary's keys
pop()             Removes the element with the specified key
popitem()         Removes the last inserted key-value pair
setdefault()      Returns the value of the specified key. If the key does not exist: insert the key, with the specified value
update()          Updates the dictionary with the specified key-value pairs
values()          Returns a list of all the values in the dictionary
```
