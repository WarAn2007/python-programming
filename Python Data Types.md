# List 
list collenction can contain same elements but in differnet index
```py
list1 = [123,321,123,'a','b', [1,2,3]]
"""
list1 contains 6 elements
int 123 stays in index[0] and [2]
list [1,2,3] in index[5]
"""
```
## 1. To Get Access and Change items
```py
list1 = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
#We are getting access to items by Index, and that is the way to change them. Index starts at 0 till infinity
print(list1[0]) #shows first item 'apple'

#We can also get items from least ( from right side)
print(list1[-1]) #shows first least item 'mango'

#we can output without any loops whole list or part of it
print(list1[:4]) #print all items until  5th element    output: ['apple', 'banana', 'cherry', 'orange']

print(list1[2:5]) # output: ['cherry', 'orange', 'kiwi']
#The search will start at index 2 (included) and end at index 5 (not included)

print(list1[2:]) #Output: ['cherry', 'orange', 'kiwi', 'melon', 'mango']
#Search from at 2 index till the end

thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list") #Output: True
```

### 1.1 Negative loop search

```py
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[-4:-1]) #output: ['orange', 'kiwi', 'melon']

```
### 1.2 Changing by Index
```py
thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"
print(thislist)   #output: ['apple','blackcurrant', 'cherry']

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
thislist[1:3] = ["blackcurrant", "watermelon"]
print(thislist)    #Output: ['apple', 'blackcurrant', 'watermelon', 'orange', 'kiwi', 'mango']

thislist = ["apple", "banana", "cherry"]
thislist[1:3] = ["watermelon"]
print(thislist)  #Output: ['apple', 'watermelon']
```
### 1.3 Inserting
Inserting is putting at specific index new item without removing items. In simple words it moves items and place at old index new item
```py
thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist)   #Output: ['apple', 'banana', 'watermelon', 'cherry']    Size increases from 3 to 4 items

```
## 2. Add and Remove items
### Adding items 2 methods
Method 1. Add to right side of list
```py
mylist = [1,2,3,4]
mylist.append(5)  # now mylist = [1,2,3,4,5]
```
Method 2. Inserting to some index
```py
mylist = [1,2,3,4]
mylist.insert(1, "cherry") # 1 shows index at which it would be located. Output: [1,"cherry",2,3,4]
```
### Removing items 4 methods
Method 1. Remove by name(variable)
```py
mylist = ["cherry", "apple", "cherry" , "banana"]
mylist.remove("cherry) # remove func deletes first appeared variable in list Output: ["apple", "cherry", "banana"]
```
Method 2. Remove by Index
```py
mylist = [1,2,3,1,4,2,1]
mylist.pop(3) #Deletes item at index 3
```
Method 3. Delete function
```py
mylist = [1,2,3,1,4,2,1]
del mylist[3] # Deletes item under index 3

del mylist   # Deletes list with all items completely
```
Method 4. Clear function
```py
mylist = [1,2,3,1,4,2,1]
mylist.clear()  # Clears list from all items (leaves empty list)
```

## 3. Loops and Comprehesions
```py
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)

print(newlist)
```
This one can be replaced with short handed
newlist = [expression for item in iterable if condition == True]
```py
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits if "a" in x]
print(newlist)

newlist = [x.upper() for x in fruits] # All items will have capital letters
```

## 4. Sorting
ist objects have a sort() method that will sort the list alphanumerically, ascending, by default:
```py
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort()
print(thislist)  # ['banana', 'kiwi', 'mango', 'orange', 'pineapple']
```
To sort descending, use the keyword argument reverse = True:
```py
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort(reverse = True)
print(thislist) # ['pineapple', 'orange', 'mango', 'kiwi', 'banana']
```
Sort the list based on how close the number is to 50:
```py
def myfunc(n):
  return abs(n - 50)

thislist = [100, 50, 65, 82, 23]
thislist.sort(key = myfunc)
print(thislist) # [50, 65, 23, 82, 100]
```
By default the sort() method is case sensitive, resulting in all capital letters being sorted before lower case letters:
```py
thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.sort(key = str.lower)  # this will sort lower cased before capital letters
print(thislist)


thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.reverse()
print(thislist)   # ['cherry', 'Kiwi', 'Orange', 'banana']

```

## 5. Join lists
```py
#Joining is the easiest part. There are 3 ways to join lists without outer libraries
list1 = [1,2,3,4]
list2 = ['cherry', 'banana','apple']

# 1 Plus Method 
x = list1 + list2
print(x) #output: [1,2,3,4,'cherry', 'banana','apple']

#2 For loop Method
for i in list2:
  list1.append(x)
print(list1) #output: [1,2,3,4,'cherry', 'banana','apple']

#3 Extend Method
list1.extend(list2)
print(list1) #output: [1,2,3,4,'cherry', 'banana','apple']
```
## 6. Methods
```txt
append()      Adds an element at the end of the list
clear()       Removes all the elements from the list
copy()        Returns a copy of the list
count()       Returns the number of elements with the specified value
extend()      Add the elements of a list (or any iterable), to the end of the current list
index()       Returns the index of the first element with the specified value
insert()      Adds an element at the specified position
pop()         Removes the element at the specified position
remove()      Removes the item with the specified value
reverse()     Reverses the order of the list
sort()        Sorts the list
```
# Tuple
A tuple is a collection which is ordered and unchangeable
# 1. Access and Change of Items
Access is same as in list, by index. We can do both positive and negative searches.
# 2. Add and Remove Items
Since we cannot change tuple collecton, we need to convert it to list to add or remove items by methods of list
```py
mytuple = (5,6,4,3,2,1)
mytuple.remove() # Error
tuple(list(mytuple).remove(6))
tuple(list(mytuple).append(7))
```
1. We convert tuple to list list(mytuple), lets say in short it is "converted_tuple"
2. Then from our 'list' we remove 6 converted_tuple.remove(6) OR add 7 converted_tuple.append(7)
3. Then we convert it again to tuple tuple(...)
# 3. Unpacking
Unpacking here is like refering items inside of tuple to some groups
```py
mytuple = ('apple','watermelon','banana')
(green, red, yellow) = mytuple
print(green,' ',red,' ',  yellow) #Output: apple watermelon banana

mytuple = ('cucumber','banana','apple','watermelon','tomato')
(green, yellow, *red) = mytuple # Asteriks (*) means choose all other that left to category 'red'
print(red,' ', green, ' ', yellow)
#Output:  ['apple', 'watermelon', 'tomato'] cucumber banana

mytuple = ('cucumber','banana','apple','watermelon','tomato')
(green, *yellow, red) = mytuple # With asteriks in this position compiler refers all items between first and last elements
print(red,' ', green, ' ', yellow)
#Output:   tomato cucumber ['banana','apple', 'watermelon']
```
# 4. Join Tuples
```py
tuple1 = ("a", "b" , "c")
tuple2 = (1, 2, 3)

tuple3 = tuple1 + tuple2
print(tuple3)
```
## OR
```py
tuple1 = ("a", "b" , "c")
tuple1 = tuple1 * 2
print(tuple1) #Output: ["a", "b" , "c","a", "b" , "c"]
```
# 5. Methods
```txt
Mostly same with list methods excluding add and remove methods
```
# Set
A set is a collection which is unordered, unchangeable*, and unindexed.
Set items are unchangeable, but you can remove items and add new items.
Sets cannot have two items with the same value
```py
set1 = {4.3,43,12,1.2,4.3, 1.2,1.2}
```
set1 becomes : {4.3,43,12,1.2}
But output is always random: {43,12,1.2,4.3}, another time {12, 1.2, 4.3,43}
True and 1 is considered the same value so set1 = {2,3,True, 1} becomes set1 = {2,3,True) 
False and 0 is considered the same value so set1 = {2,3,False, 0} becomes set1 = {2,3,False) 
# 1. Access
```py
thisset = {"apple", "banana", "cherry"}
for x in thisset:
  print(x)

print("banana" in thisset) #True
print("banana" not in thisset) #False
```
# 2. Add Set Items ☻
```py
thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}

thisset.update(tropical) # <- means thisset was enlarged with data of tropical

# This actualy helps to avoid repeating words to do a list of all existing items, like
fruits = {}
national = {...}
tropical = {...}
exotic = {...}
fruit.update(national)
fruit.update(tropical)
fruit.update(exotic)
print(fruit) # Will show all fruits without duplicates but without order 
```
OR simply use .add() method
```py
thisset = {2,3,4,5}
thisset.add(9) # thisset = {2,3,4,5,9}
```
# 3. Remove Set Items
## 1) Remove ( If items doesn't exist in set, compiler will raise an ERROR )
```py
thisset = {"apple", "banana", "cherry"}
thisset.remove("watermelon") # ERROR
thisset.remove("banana") # {'apple','cherry'}
```
## 2) Discard ( If items doesn't exist in set, compiler will NOT raise an ERROR )
```py
thisset = {"apple", "banana", "cherry"}
thisset.discard("watermelon") # {'banana', 'cherry', 'apple'}
thisset.discard("banana") # {'apple','cherry'}
```
## 3) Pop ( It is the way delete random item from set, because set is always unordered )
```py
thisset = {"apple", "banana", "cherry"}
x = thisset.pop()
print(x) # Shows removed item
print(thisset) # Shows the set without deleted item
```
## 4) Clear ( Clears  set massive )
```py
thisset = {"apple", "banana", "cherry"}
thisset.clear()
```
## 5) Del ( Deletes set massive )
```py
thisset = {"apple", "banana", "cherry"}
del thisset
```
# 4. Join Sets
## 1) Union, Update and operator | ( Joins two sets)
#### ! Union function allows to join set with other massive types(list, tuple)                                !
#### ! Update function doesn't save join of two sets into new one, instead it fulfills first set with another !
#### ! Operator | allows to join multiple sets                                                                !
```py
thisset1 = {"apple", "banana", "cherry"}
thisset2 = {3,2,4}
union_method = thisset1.union(thisset2)
operator_method = thisset1 | thisset2
thisset1.update(thisset2)
```
## 2) Symmetric Difference ( This  method will keep only the elements that are NOT present in both sets )

```py
thisset1 = {"apple", "banana", "cherry"}
thisset2 = {3,2,4, "apple"}
set3 = thisset1.symmetric_difference(thisset2)
set4 = thisset1 ^ thisset2
print(set3) # {'banana', 'cherry',3,4,2}
print(set4) # {'banana', 'cherry',3,4,2}
```
## 3) Intersection and & (This method will return a new set, that ONLY contains the items that are present in both sets )
#### ! Operator & will show the save result but is able to hold multiple sets !
```py
thisset1 = {"apple", "banana", "cherry"}
thisset2 = {3,2,4, "apple"}
set3 = thisset1.intersection(thisset2)
set4 = thisset1 & thisset2
print(set3) # {'apple'}
print(set4) # {'apple'}
```
## 4) Difference and - ( This method will return a new set that will contain only the items from the first set that are not present in the other set)
#### ! Operator '-' will show the same result !
```py
thisset1 = {"apple", "banana", "cherry"}
thisset2 = {3,2,4, "apple"}
set3 = thisset1.difference(thisset2)
set4 = thisset1 - thisset2
print(set3) # {'banana', 'cherry'}
print(set4) # {'banana', 'cherry'}
```
# 5. Frozenset
#### frozenset is an immutable version of a set. 
#### Use the frozenset() constructor to create a frozenset from any iterable
#### Being immutable means you cannot add or remove elements. However, frozensets support all non-mutating operations of sets.
```txt
METHODS             SHORTCUTS       MEANINGS
copy()                            Returns a shallow copy	
difference()             -	      Returns a new frozenset with the difference	
intersection()           &	      Returns a new frozenset with the intersection	
isdisjoint()                      Returns whether two frozensets have an intersection	
issubset()               <= / <   Returns True if this frozenset is a (proper) subset of another	
issuperset()             >= / >   Returns True if this frozenset is a (proper) superset of another	
symmetric_difference()   ^        Returns a new frozenset with the symmetric differences	
union()                  |        Returns a new frozenset containing the union
```
# 6. Methods
```txt
add()                            Adds an element to the set
clear()                          Removes all the elements from the set
copy()                           Returns a copy of the set
difference()                     Returns a set containing the difference between two or more sets
difference_update()              Removes the items in this set that are also included in another, specified set
discard()                        Remove the specified item
intersection()                   Returns a set, that is the intersection of two other sets
intersection_update()            Removes the items in this set that are not present in other, specified set(s)
isdisjoint()                     Returns whether two sets have a intersection or not
issubset()                       Returns True if all items of this set is present in another set
issuperset()                     Returns True if all items of another set is present in this set
pop()                            Removes an element from the set
remove()                         Removes the specified element
symmetric_difference()           Returns a set with the symmetric differences of two sets
symmetric_difference_update()    Inserts the symmetric differences from this set and another
union()                          Return a set containing the union of sets
update()                         Update the set with the union of this set and others
```
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
Update method ( if exist key, update it. Else add new)
```py
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})
thisdict.update({"color": "red"})
```
Direct change ( if exist key, change it. Else add new)
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
# 4. Nested Dictionaries
