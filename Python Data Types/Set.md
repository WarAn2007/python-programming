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
