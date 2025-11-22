# List 
## 1. Data type list contains different elements and differnt data types under specific index. List can contain same elements as well but in differnet index
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
###2.2 Changing by Index
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
###2.3 Inserting
```py
#Inserting is putting at specific index new item without removing items. In simple words it moves items and place at old index new item
thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist)   #Output: ['apple', 'banana', 'watermelon', 'cherry']    Size increases from 3 to 4 items

```
## 3. Add and Remove items
## 4. Loops and Comprehesions
## 5. Sorting
## 6. Join lists
## 7. Methods


# Tuple

# Set

# Dictionary( Dict)

# Array
