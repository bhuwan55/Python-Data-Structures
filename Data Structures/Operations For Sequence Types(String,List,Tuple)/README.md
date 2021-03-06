# 1. Indexing:
* Accessing any item in sequence using it's index.
* Starts with 0 for the first item. So **fourth element is 3 i.e [4-1]**
* Can be accessed using square bracket **[index_numer]**

For example. Consider the following example:

## 1.1 Indexing String
```python

# String 
x = "surya"
print(x[3]) # output = y
``` 

## 1.2 Indexing List
```python

# list
x = ['surya','ramesh','kiran']
print(x[1]) # output = ramesh

```        

## 1.3 Indexing Tuples
```python
#tuple
x = ('surya','ramesh','kiran')
print(x[1]) # output = ramesh
```

# 2.Slicing
* Slices out substring, substring, subtuples, using indexes.
* **Syntax : [start:end+1:step]**. ``Mathematical equivalence of indexing: [start,end)``    

## 2.1 Slicing Of String:
```python
# indexing of string
x = "computer"
```
**Index provided:**

| Letter   |      From Left     |  From Right |
|----------|:------------------:|------------:|
|   c      |      0             |    -8       |
|   o      |      1             |    -7       |
|   m      |      2             |    -6       |
|   p      |      3             |    -5       |
|   u      |      4             |    -4       |
|   t      |      5             |    -3       |
|   e      |      6             |    -2       |
|   r      |      7             |    -1       |


``` python
"""from 1st index to 3rd index"""
print(x[1:4])  # omp
```

```python
"""from 1st index to 5th index with step of 2"""
print(x[1:6:2])  # opt
```

```python
"""From 3rd index to last index"""
print(x[3:])  # puter
```

```python
"""Last element indexing"""
print(x[-1])  # r
```

```python
"""third last to last index"""
print(x[-3:])  # ter
```

```python
"""from first index to third last"""
print(x[:-2]) # comput
```

```python
"""First element accessed from right"""
print(x[-8]) # c
```

* ``If start is not declared, it's value is set to zero`` 
* ``If end is not declared, it's value is set to length.``
* ``If step is not declared, it's value is set to 1.``

**Note: Slicing of tuples,list is same as that of string.** 

# 3. Concatenating
* Combining of two same data types into one.
* Often achieved by using **+** sign. i.e <var1>+<var2>

## 3.1 Concatenating of Strings:
```python
# string
x = "This is"
y = "going to be con-catinated."
print(x+y) # This is going to be con-catinated. 
```

## 3.2 Concatenating of List: 
```python
#list
x = ["This","is"]
y = ["going", "to","be","contatinated."] # ["This","is","going", "to","be","contatinated."]
print(x+y)
```

## 3.3 Concatenating of Tuple:
```python
#tuple
x = ('Hello','')
y = ('Hi','') # ('Hello','','Hi','')
print(x+y)
```
**If defining tuples with one item use ",""** i.e

```python
x = ("hi",)  
y = ("hello",)
print(x+y)
```  

# 4. Multiplying:
* Repeated adding of self for number of times.
* Achieved using ```*``` sign. i.e <data_type>*3

## 4.1. Multiplying of String:
```python
#string:
x = "a"*3
print(x) # aaa
```

## 4.2. Multiplying of List:
```python
#list
x = ["hi"]
print(x*3) # ["hi","hi","hi"] 
```
## 4.3. Multiplying of Tuple:
```python
#tuple:
x =("hi",)
print(x*3) # ('hi', 'hi', 'hi')
```

# 5. Checking Membership
* Tests weather an item is or not in sequence.

* *Syntax1*: ```item in <variable_name> ``` Returns : **true if exists**,**false if doesn't exists**.
* *Syntax2*: ```item not in <variable_name> ``` Returns : **false if exists**,**true if doesn't exists**.

## 5.1 String
```python
#string
x = "surya"
print("u" in x)  # true
```

## 5.2 List
```python
#list
x = ["surya","ramesh","kiran"]
print("asd" in x)  # false
```

## 5.3 Tuple
```python
#tuple
x = (1,2,3)
print(1 in x)  # true
```

# 6. Iterating
* Iterating through the items in sequence:
* Index and item can be evaluated by passing 
the variable to inbuilt function **enumerate.**  

## 6.1 Iterating through String:
```python
# string enumeration
s = "hello"
for index,item in enumerate(s):
    print("item={item}, index={index}".format(item=item,index=index))
```  

**Output:**
```
tem=h, index=0
item=e, index=1
item=l, index=2
item=l, index=3
item=o, index=4
```
## 6.2 Iterating through list:
```python
x = ["hello","hi"]
for index,item in enumerate(x):
    print("item={item}, index={index}".format(item=item,index=index))
```  

**Output:**
```
item=hello, index=0
item=hi, index=1
```

## 6.3 Iterating through Tuples:
```python
# tuple enumeration
y = (9,8,4,3,1,2)
for index,item in enumerate(y):
    print("item={item}, index={index}".format(item=item,index=index))
```
**Output:**
```
item=9, index=0
item=8, index=1
item=4, index=2
item=3, index=3
item=1, index=4
item=2, index=5
```

# 7. Number of Items:
* Count the number of item in sequence.
* Basically inbuilt function **len()** in used.
* *Syntax*: len(variable_name)

## 7.1 String:
```python
x = "hello, this is me"
print(len(x))  # counts the space too.
```

**Output:** ``17``
> Counts the spaces too

## 7.2 Lists:
```python
# list
y = ["hello","this","is","me"]
print(len(y))
```

**Output:** ``4``

``Note: Same is in the case of tuple``

# 7. Minimum
* finds the minimum item in sequence [lexicographically](https://en.wikipedia.org/wiki/Lexicographical_order).
* Alphabetic **or** numeric types. But cannot be mixed. 
> Caution !: Not to be used in mixed data types. eg. in case of list [1,"string"].


 
## 7.1 Minimum Element in String:
```python
#string
x = 'hello'
print(min(x))
```

**Output :** ``e``. Because e < h < l < o in lexicographic ordering.

## 7.2 Minimum Element in List:
```python
#list
y = [9,2,6,1,0]
print(min(y))
``` 
**Output :** ``0``

## 7.3 Tuple:
```python
#tuple
y = ('@','#','$','a')
print(min(y))
```
**Output:** ``#``.  Because the ASCII value of # is comparatively smaller.i.e
``ASCII(#) < ASCII(@) < ASCII($) < ASCII(a)``

# 8. Maximum:
* finds the maximum item in sequence [lexicographically](https://en.wikipedia.org/wiki/Lexicographical_order).
* Alphabetic **or** numeric types. But cannot be mixed.
* *Syntax:* max(variable)

```python
x = "abcde"
print(max(x)) 
```
**Output:** ``e``

*Similar to min in case of list and tuples data types.*


# 9. Sum
* Finds the sum of items in sequence.
* Entire sum must be numeric.

## 9.1 Sum of elements in list:
```python
# list
x = [1,2,3,4,5]
print(sum(x))  # 15
print(sum(x[-2:]))  # 4+5 = 9
print(sum(x[0:4:2]))  # 1+3 = 4
```

## 9.2 Sum of elements in tuples:
```python
# tuples
x = (5,6,7,8)
print(sum(x)) # 5+6+7+8 = 26
print(sum(x[0:3:2]))  # 5+7 = 12
```

# 10. Sorting
* Returns a new list of items sorted in order.
* Does not changes the original list.

## 10.1 Sorting Of String:
```python
x = "hello"
print(sorted(x))
```
**Output** : ``['e', 'h', 'l', 'l', 'o']``

## 10.2 Sorting Of List:
```python
y = ["dat","rat","apple"]
print(sorted(y))
```
**Output** : ``['apple', 'dat', 'rat']``

## 10.3 Sorting Of Tuples:
```python
z = (5,3,1,8,6)
print(sorted(z))
```
**Output** : ``[1, 3, 5, 6, 8]``

**Note:** For every data type, a resulting data type after sorting is list.

# 11. Sorting by second letter
* Add a key parameter lambda function to return the second character.

```python
x = ["Kelvin","Niklas","Jenny","Craig"]
print(sorted(x, key=lambda k: k[1]))
``` 
**Output:** ``['Kelvin', 'Jenny', 'Niklas', 'Craig']``

**The word *key* here is defined parameter name for inbuilt function *sorted()*,
 k is arbitart variable name**

Lambda is a inbuilt [functional programming]((https://kite.com/blog/python/functional-programming/)) 
keyword in python.

**Same applies for tuples and other data structures.**

# 12. Count of item:
* Counts the item in the data structure.
* *Syntax*: var_name.count(item)
* Basically *count()* is the member function of the pre-defined data-structure.

## 12.1 Counting of item in string
```python
x = "hippo"
print(x.count("p"))
```
**Output:** ``2``

## 12.2 Counting of item in List
```python
y = ['@','$','*','p','#','#','$','#']
print(y.count("#"))
```
**Output:** ``3``

## 12.2 Counting of item in Tuple
```python
z = (1,2,3,1,1,2,4,1)
print(z.count(1))
```
**Output:** ``4``

# 13. Index Of Item
* Returns the **index of the first occurance** of item.
* *Syntax:* var_name.index(item)
* `index()` function is member function of the inbuilt data structure. 

## 13.1 Indexing Of String:
```python
x = "qweert"
print(x.index("e"))
```

**Output:** ``2``

## 13.2 Indexing Of List:
```python
x = ["cat","tiger","cat","rat"]
print(x.index("cat"))
```

**Output:** ``0``

## 13.3 Indexing of Tuple:
```python
z = (0,1,1,2,3,4)
print(z.index(1))
```
**Output:** ``1``

