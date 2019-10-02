CSCI 2270 Final
===============
Directions
----------
**Read these directions carefully.**
You will be solving two of the three programming problems detailed below. _Problem 1_ is **mandatory**, but you only have to do **either** _Problem 2_ **or** _Problem 3_. For each problem you must submit three documents:

1. A C++ program that solves the given problem. It is required that your code files are well commented. `Note: you will not receive more than 25% of the possible points on any problem if your submitted code does not compile.`
2. If your code does not fully meet the specifications, then include a text file with your explanations for potential partial credit.

The third document you submit will help us understand your thought process. Mention anything you have done to write, test, and debug your code. Incomplete code can still receive points if you show that you have identified the errors and tried to debug them.
* Your submission should be valid C++ 11 code.
* Your solutions should use similar types and functions to the example code provided, but you are welcome to make modifications as you see fit.
* Show how you have tested your code. You will be graded higher for code with complete tests.
* We will be running this code on other computers, so make sure to avoid **any** undefined behavior such as uninitialized variables.

<div style="page-break-after: always;"></div>

Problem 1 (Mandatory)
---------------------

### Task:
Given a linked list, remove the n-th node from the end of list and return its head (n is a positive number and no larger than of the length of the linked list)

### Requirements:
Implement a `removeNthFromEnd` function: _(You must not change anything in hpp file. You may add helper function in the cpp as required)_
  ```cpp
  Node* LinkedList::removeNthFromEnd(int n);
  ```
  This function should delete the nth node from the end in a linked list and return the head of the new linked list.

### Examples:
**Example 1**:
* If the original linked list (_original_LL_) is-
   ```
   10 -> 20 -> 30 -> 40 -> NULL
   ```

   After passing it through the function `removeNthFromEnd`, for example,
    
   `original_LL.removeNthFromEnd(2)`
   
   the linked list should become:
   ```
   10 -> 20 -> 40 -> NULL
   ```
   Because the 2nd node from the end is 30 so we should remove 30. 
   

**Example 2**:

* If the original linked list(_original_LL_) is-

   ```
   10 -> 20 -> 40  -> NULL
    ```

   After passing it through the function `removeNthFromEnd`, for example,
       
  `original_LL.removeNthFromEnd(1)`
      
   the linked list should become:
   ```
   10 -> 20 -> NULL
   ```
   Because the 1st node from the end is 40 so we should remove 40.
   
 Hint:
1. **Test your function** to make sure that it works in every case, especially the edge cases like n = 1 or n = the length of linked list.

2. One possible way to do this: 

    You can use two seperate pointers(e.g. _prev_ and _pres_) if needed; 
    
    Move _pres_ n nodes after _prev_ ;
    
    Then move them together until the fast pointer(_pres_) reaches the end; 
    
    Now the slow pointer(_pres_) will point to the nth node from the end; 
    
    Delete the required node and return the head.

<div style="page-break-after: always;"></div>



Problem 2
----------

### Task:
 In this assignment you will create a Queue with __stack(s)__. Stack class implementation is complete. __You do not have to do any implementation for stack class__.  Most of the functions for the queue are also implemented in the ```.cpp``` file. __You need to implement the dequeue function. You will use methods of stack class to implement the dequeue function in the queue class.__

### Requirements:

The dequeue function will have following signature
```cpp
int Queue:: dequeue()
```
The function will dequeue element at the front of the queue and will return that value. If the queue is empty dequeue should print ``Queue is empty. Can not dequeue`` and return ``-999``.

 You are supposed to implement queue using stack. So you can use push, pop, peek functions of the member stack(s) of your queue.
  * __Do not access element by array indices inside the dequeue function__.
  * __Do not use any other data structure than stack to implement this queue__.


### EXAMPLE (Hint)
Let's assume we will enqueue < 1, 2, 3, 4 > in the order mentioned. 1 will be enqueued first. Then 2 will enqueued and so on. Following image shows the state of the member stacks after enqueue. Note 4 is towards the top of the stack and 1 is at the bottom.
<img src="enQ.png"
   alt="Markdown Monster icon"
   style="float: left; margin-right: 10px;" />

However, when we will dequeue we need to return 1. Recall that queue is First in First out. So if we dequeue we should get 1 first. Next dequeue should return 2. Third dequeue should return 3 and so on. FOllowing image shows the how can you acheive such result using the secondary stack.
<img src="deQ.png"
   alt="Markdown Monster icon"
   style="float: left; margin-right: 10px;" />



2. **Test your function** to make sure that it passes all the test cases.

<div style="page-break-after: always;"></div>


Problem 3
----------

### Task:
Write a program that deletes all the duplicates from a linked list. Assume that the list is unsorted.

### Requirements:

1. Implement a `deleteDuplicates` function: _(You must not change anything in hpp file. You may add helper function in the cpp as required)_
  ```cpp
  void deleteDuplicates();
  ```
  This function should delete all the duplicate items in a linked list.
  If the list is empty, print 'Empty List' inside the function.

 **Examples:**

   * If the list is-
   ```
   10 -> 20 -> 30 -> 40 -> NULL
   ```

   After passing it through the function, it should still remain:
   ```
   10 -> 20 -> 30 -> 40 -> NULL
   ```

   * If the list is-
 ```
 10 -> 20 -> -30 -> 20 -> -30 -> 10 -> NULL
  ```

   After passing it through the function, it should change to:
   ```
   10 -> 20 -> -30 -> NULL
   ```

   * If the list is-
   ```
   5 -> 5 -> 5 -> NULL
   ```
   After passing it through the function, it should change to:
   ```
   5 -> NULL
   ```

2. A small driver is given as `main.cpp`. Feel free to add testcases suitable for your problem.

3. **Test your function** to make sure that it works in every case, no matter how many items are there in the LinkedList.
