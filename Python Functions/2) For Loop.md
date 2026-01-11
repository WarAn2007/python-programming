# Loop functions
## For Loop
```py
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)  #output : apple banana cherry

for x in range(6):
  print(x)  #output (from 0 to 6 except 6 itself): 0 1 2 3 4 5

for x in range(2,6):
  print(x)  #output (from 2 to 6 except 6 itself) : 2 3 4 5

for x in range(2, 33, 3):
  print(x) #prints each 3rd number from 2 'till 33 except 33 itself
# output : 2 5 8 11 14 17 20 23 26 29 32
 
for x in range(6):
  print(x)
esle:
  print("Programm finished")  #output : 0 1 2 3 4 5 Programm finished

for x in range(6):
  print(x)
  if x == 2:
    break
esle:
  print("Programm finished")  #output : 0 1 2    | else doesn't executes if programm "breaks"

for x in "banana":
  print(x)  #output : b a n a n a
```
## 1.1 Using if/else in for loop
```py
for x in range(6):
  print(x)
  if x == 3:
  break #output: 0 1 2 3    Break func executes when x == 3

# If you switch print and if func output will be like : 0 1 2
for x in range(6):
  if x == 3:
    break
  print(x)

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x)
# With the continue statement we can stop the current iteration of the loop, and continue with the next:

#output: apple cherry
```
## 1.2 Nested loop
```py
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)
*** Output: 
red apple
red banana
red cherry
big apple
big banana
big cherry
tasty apple
tasty banana
tasty cherry
***
```
