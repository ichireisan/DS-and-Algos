# DS and Algos
This document will serve as a cheatsheet for learning Data Structures and Algorithms

A **Data Structure** is an algebraic structure about data.  
ie  
&emsp; {&emsp; [A Collection of data points in a certain format],  
&emsp;&emsp;&emsp;&emsp;[various operations that can be performed on that collection],  
&emsp;&emsp;&emsp;&emsp;[Rules the operations must satisfy] &emsp;}
 
## Abstract Data Structures

&emsp; Basic
- Boolean
- Number - Integer/Float
- String - Character(s)

&emsp; Linear - A data structure whose elements form a sequence.
- List
- Stack
- Queue
- Priority Queue
- Double-ended Queue
- Double-ended Priority Queue

&emsp; Associative
- Set
- MultiSet
- Map/Dictionary
    
&emsp; Graphs
- Trees
#### What is it?

#### Operations

#### Pythonic Implementation

###List
#### What is it?
&emsp; &emsp; It is a finite number of ordered values, where the same value may occur more than once   


<table>

<tr>
<td> Operations </td> <td> Pythonic Implementation </td>
</tr>

<tr>
<td> create an empty list </td>
<td>
    
```python
my_list = []
```

</td>
</tr>

<tr>
<td> check if list is empty </td>
<td>
    
```python
if not my_list:
    print("my_list is empty")
```
    
</td>
</tr>

<tr>
<td> prepend to list </td>
<td>
    
```python
my_list.insert(item)
```
    
</td>
</tr>

<tr>
<td> append to list </td>
<td>
    
```python
my_list.append(item)
```
    
</td>
</tr>

<tr>
<td> what is the first/head item in the list </td>
<td>
    
```python
my_list[0]
or
my_list.pop()
```
    
</td>
</tr>

<tr>
<td> what is the last item in the list </td>
<td>
    
```python
my_list[-1]

```
    
</td>
</tr>

<tr>
<td> Skip the head & get the rest </td>
<td>
    
```python
my_list[1:]
```
    
</td>
</tr>

<tr>
<td> Whats the item at nth index </td>
<td>
    
```python
my_list[n]
```
    
</td>
</tr>

</table>


