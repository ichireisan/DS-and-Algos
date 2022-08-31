# Data Structures and Algorithms

---
This document will serve as a cheatsheet for learning Data Structures and Algorithms

A **Data Structure** is an algebraic structure about data.  
ie  
&emsp; { [A Collection of data points in a certain format],  
&emsp;&emsp;&emsp;[various operations that can be performed on that collection],  
&emsp;&emsp;&emsp;[Rules the operations must satisfy] }
--- 
## Abstract Data Structures

- Basic
    - Boolean
    - Number - Integer/Float
    - String - Character(s)

- Linear - A data structure whose elements form a sequence.
    - List
    - Linked List
    - Stack
    - Queue
    - Priority Queue
    - Double-ended Queue
    - Double-ended Priority Queue

- Associative
    - Set
    - MultiSet
    - Map/Dictionary
    
- Graphs
    - Trees

---

As per The Mathematical Theory of Communication, the smallest unit which can be used to convey 
information is called a Shannon or bit. That is either a 0 or 1 can be used to make any meaning, 
language or whatever. So, the smallest data type or data structure happens to be a Boolean.

0 or 1 may be used to represent numbers, text, emojis or any other advanced form of data like audio, 
video, photos, etc in different types of data structures.

Numbers are either Integer or Float.  
Text, aka string, is either a character or a list of characters.

Numbers and text have their own set of Operations.

#### Typical Operations on a Data Structure
- Initialize/Create the Data Structure
- Add/Delete elements to/from the structure
- Traverse/navigate/Search/filter the structure
- check if the structure is empty or full.

###List

&emsp; &emsp; is a collection of finite number of ordered data, where the same data 
may occur more than once.   


<table>

<tr>
<td> <b>Operations</b> </td> <td> <b>Pythonic Implementation </b> </td>
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
<td> What is the item at nth index </td>
<td>
    
```python
my_list[n]
```
    
</td>
</tr>

</table>

---
### Linked List
&emsp; &emsp; is a series of connected data nodes where each data node stores the data and 
the address(es) of other node(s) to which it connects.

&emsp; &emsp; A node may connect to none, itself, one or more nodes.

&emsp; &emsp; Used for building other Data Structures like Stacks, Queue, List, Trees, Graphs.

&emsp; &emsp; Linked List has different kinds of Operations depending on which other data structure it would be used to make.


&emsp; &emsp; **Basic Pythonic Implementation**
```python
class Node:

    def __init__(self, item):
        self.item = item
        self.next = None


class LinkedList:

    def __init__(self):
        self.head = None # head value will be set with an instance of Node()

if __name__ == '__main__':

    linked_list = LinkedList()

    linked_list.head = Node(1)
```


---

### Stack
&emsp; &emsp; aka LIFO, is a collection where a data element is added or removed only from the top of the list.


<table>

<tr>
<td> <b>Operations</b> </td> <td> <b>Pythonic Implementation </b> </td>
</tr>

<tr>
<td> Create a stack </td>
<td>
    
```python
class Node:
      
    def __init__(self,data):
        self.data = data
        self.next = None
      
class Stack:
      
    def __init__(self):
        self.head = None
        
my_stack = Stack()

```

</td>
</tr>

<tr>
<td> Push | Add an entry to the top/head/front of the list </td>
<td>
    
```python
class Stack:
    def push(self,data):
              
        # If stack is empty, add Node to head.    
        if self.head == None: 
            self.head=Node(data)
        
        # Else move current head to the next node (the node below in Stack)
        else: 
            newnode = Node(data)
            newnode.next = self.head
            self.head = newnode
```

</td>
</tr>

<tr>
<td> Pop | Remove an entry from top/head/front of the list </td>
<td>
    
```python
class Stack:
...
    def pop(self):
              
        if self.isempty():
            return None
              
        else:
            # Get the current head, then it's next Node and set it as the current head.
            poppednode = self.head
            self.head = self.head.next
            poppednode.next = None
            return poppednode.data
```

</td>
</tr>

<tr>
<td> IsEmpty | Check if the stack is empty </td>
<td>
    
```python
class Stack:
...
    def isempty(self):
        if self.head == None:
            return True
        else:
            return False
```

</td>
</tr>

<tr>
<td> IsFull | Check if the stack is full </td>
<td>
    
```python

```

</td>
</tr>


<tr>
<td> Peek | Get the value of the top element without removing it</td>
<td>
    
```python
class Stack:
...
    def peek(self):
          
        if self.isempty():
            return None
              
        else:
            return self.head.data
```

</td>
</tr>

</table>
    
---

### Queue

&emsp; &emsp; aka FIFO, is a sequence where data elements are added from one end and removed from the other.  
&emsp; &emsp; In a queue, the end where data enters is called **Front**. The end where data is removed is called **Rear**.

<table>

<tr>
<td> <b>Operations</b> </td> <td> <b>Pythonic Implementation </b> </td>
</tr>

<tr>
<td> Create a Queue </td>

<td>

```python
class Node:
      
    def __init__(self, data):
        self.data = data
        self.next = None
  
class Queue:
      
    def __init__(self):
        self.front = self.rear = None

q = Queue()
```

</td>

</tr>


<tr>
<td> Add to a Queue </td>

<td>

```python
class Queue:
...
    # Create a node
    # if queue is empty, set front and read of queue as the created node
    # else, Set the rear and rear's next node as the created node.
    def EnQueue(self, item):
        temp = Node(item)
          
        if self.rear == None:
            self.front = self.rear = temp
            return
        self.rear.next = temp
        self.rear = temp
```

</td>

</tr>

<tr>
<td> Remove from Queue </td>

<td>

```python
class Queue:
...
    # if Queue is empty, just return
    # Else set the current front as current front's next.
    # And then if current front is None, then set the rear also as None as the queue has become empty.
    def DeQueue(self):
          
        if self.isEmpty():
            return
        temp = self.front
        self.front = temp.next
  
        if(self.front == None):
            self.rear = None
```

</td>

</tr>


<tr>
<td> Is the Queue Empty </td>

<td>

```python
class Queue:
...
    # Return True if current front is None.
    def isEmpty(self):
        return self.front == None
```

</td>

</tr>

</table>