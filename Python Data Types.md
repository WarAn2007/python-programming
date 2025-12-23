# List 
## 1. list collenction can contain same elements but in differnet index
```py
list1 = [123,321,123,'a','b', [1,2,3]]
"""
list1 contains 6 elements
int 123 stays in index[0] and [2]
list [1,2,3] in index[5]
"""
```
## 2. To Get Access and Change items
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

### 2.1 Negative loop search

```py
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[-4:-1]) #output: ['orange', 'kiwi', 'melon']

```
### 2.2 Changing by Index
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
### 2.3 Inserting
```py
#Inserting is putting at specific index new item without removing items. In simple words it moves items and place at old index new item
thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist)   #Output: ['apple', 'banana', 'watermelon', 'cherry']    Size increases from 3 to 4 items

```
## 3. Add and Remove items
```py
#Adding items 2 methods
#Method 1. Add to right side of list
mylist = [1,2,3,4]
mylist.append(5)  # now mylist = [1,2,3,4,5]

#Method 2. Inserting to some index
mylist = [1,2,3,4]
mylist.insert(1, "cherry") # 1 shows index at which it would be located. Output: [1,"cherry",2,3,4]


#Removing items 4 methods
#Method 1. Remove by name(variable)
mylist = ["cherry", "apple", "cherry" , "banana"]
mylist.remove("cherry) # remove func deletes first appeared variable in list Output: ["apple", "cherry", "banana"]

#Method 2. Remove by Index
mylist = [1,2,3,1,4,2,1]
mylist.pop(3) #Deletes item at index 3

#Method 3. Delete function
mylist = [1,2,3,1,4,2,1]
del mylist[3] # Deletes item under index 3

del mylist   # Deletes list with all items completely

#Method 4. Clear function
mylist = [1,2,3,1,4,2,1]
mylist.clear()  # Clears list from all items (leaves empty list)
```

## 4. Loops and Comprehesions
```py
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)

print(newlist)

# This one can be replaced with short handed
# newlist = [expression for item in iterable if condition == True]

fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits if "a" in x]
print(newlist)

newlist = [x.upper() for x in fruits] # All items will have capital letters

```

## 5. Sorting
```py
# List objects have a sort() method that will sort the list alphanumerically, ascending, by default:

thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort()
print(thislist)  # ['banana', 'kiwi', 'mango', 'orange', 'pineapple']

# To sort descending, use the keyword argument reverse = True:

thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort(reverse = True)
print(thislist) # ['pineapple', 'orange', 'mango', 'kiwi', 'banana']

# Sort the list based on how close the number is to 50:
def myfunc(n):
  return abs(n - 50)

thislist = [100, 50, 65, 82, 23]
thislist.sort(key = myfunc)
print(thislist) # [50, 65, 23, 82, 100]


# By default the sort() method is case sensitive, resulting in all capital letters being sorted before lower case letters:
thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.sort(key = str.lower)  # this will sort lower cased before capital letters
print(thislist)


thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.reverse()
print(thislist)   # ['cherry', 'Kiwi', 'Orange', 'banana']

```

## 6. Join lists
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
## 7. Methods
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
"""
1. We convert tuple to list list(mytuple), lets say in short it is "converted_tuple"
2. Then from our 'list' we remove 6 converted_tuple.remove(6) OR add 7 converted_tuple.append(7)
3. Then we convert it again to tuple tuple(...)
"""
```
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
set1 = {4.3,43,12,1.2,4.3, 1.2,1.2) # Is stored like set1 =set1 = {4.3,43,12,1.2)
```
True and 1 is considered the same value so set1 = {2,3,True, 1} becomes set1 = {2,3,True) 
False and 0 is considered the same value so set1 = {2,3,False, 0} becomes set1 = {2,3,False) 
# 1. Access
```py

```
# Dictionary( Dict)

# Array
