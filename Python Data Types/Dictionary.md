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
# 4. Nested Dictionaries
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
