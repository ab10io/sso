CSCI 2270 Final
===============

Directions
----------
**Read these directions carefully.**
You will be solving two of the three programming problems detailed below. _Problem 1_ is **mandatory**, but you only have to do **either** _Problem 2_ **or** _Problem 3_. For each problem you must submit three documents:

1. A C++ program that solves the given problem.
2. A text file that contains the output of your program when it is run.
3. A short document that contains any issues or concerns you have about the given problem, as well as any information that we need to understand, compile, or run your solution.

The third document you submit will help us understand your thought process. Mention anything you have done to write, test, and debug your code. Incomplete code can still receive points if you show that you have identified the errors and tried to debug them.

* Your submission should be valid C++ 11 code.
* Your solutions should use similar types and functions to the example code provided, but you are welcome to make modifications as you see fit.
* Show how you have tested your code. You will be graded higher for code with complete tests.
* We will be running this code on other computers, so make sure to avoid **any** undefined behavior such as uninitialized variables.

<div style="page-break-after: always;"></div>

Problem 1
----------------------

### Task:
Find the middle of a given linked list in C++. Given a singly linked list, find middle of the linked list. For example, if given linked list is 1->2->3->4->5 then output should be 3. If there are even nodes, then there would be two middle nodes, we need to print second middle element. For example, if given linked list is 1->2->3->4->5->6 then output should be 4.

### Requirements:
1. Implement a `getMiddle` function:
  ```
  Node*  getMiddle();
  ```
  This function should return the middle node.

  **Examples:**  
    * Calling `getMiddle`  on linkedList  1->2->3->4->5->6  should return 3  

	* Calling `getMiddle`  on linkedList  1->2->3->4->5  should return 3  

      ![Example  image](Capture.png)


2. **Test your function** Test your code against the test cases given in the code.

<div style="page-break-after: always;"></div>



Problem 2
---------

### Task:
Find the middle of a given linked list in C++. Given a singly linked list, find middle of the linked list. For example, if given linked list is 1->2->3->4->5 then output should be 3. If there are even nodes, then there would be two middle nodes, we need to print second middle element. For example, if given linked list is 1->2->3->4->5->6 then output should be 4.

### Requirements:
1. Implement a `inefficientGetMiddle` function:
  ```
  Node* inefficientGetMiddle();
  ```
  This function should return the middle node.

  **Examples:**  
    * Calling `inefficientGetMiddle`  on linkedList  1->2->3->4->5->6  should return 3  

	* Calling `inefficientGetMiddle`  on linkedList  1->2->3->4->5  should return 3  


2. **Test your function** Test your code against the test cases given in the code.

<div style="page-break-after: always;"></div>
