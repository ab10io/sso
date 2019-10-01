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
Problem 1 (Mandatory)
---------------------
### Task:
Given an array of integers and a target number, determine which two integers from the list (if any) can be added to reach the target number. This must be done efficiently, in O(n) time, by using a hash table.
### Requirements:
1. Implement a `printIndicesOfSum` function:
  ```cpp
  void printIndicesOfSum(vector<int> arr, int target); // example declaration
  ```
  This function should determine which two integers in `arr` add up to `target`, and if they exist it should print their indices. It should do this in O(n) time by using a hash table, although the exact implementation is left to you to decide.  
  _Hint: storing every number in a hash table will reduce the time it takes to search for a specific number from O(n) to O(1)._
  **Examples:**  
  * Given the array `[9, 5, 7, 19]` and the target `24`, calling `printIndicesOfSum(arr, target)` should print `Indices 1 and 3 sum to 24`.  
  * Given the array `[1, 7, 6, 2]` and the target `8`, calling `printIndicesOfSum(arr, target)` should print either `Indices 0 and 1 sum to 24` or `Indices 2 and 3 sum to 24`. Both are valid.  
  * Given the array `[1, 2, 6, 2]` and the target `12`, calling `printIndicesOfSum(arr, target)` should print `No indices sum to 12`.  
2. Write a main function that creates an array of integers, then calls the function defined in part (1) to determine which two indices sum to a particular target. Call it on multiple lists and with multiple targets to show that it works in all cases, and print out the results.
3. **Test your function** to make sure that it works in every case, no matter which values are passed in.
<div style="page-break-after: always;"></div>
Problem 2
----------
### Task:
You are required to process a given string S that includes '#' symbol. The '#' symbol represents backspace of a character. For instance given a string 'abc#def' you are required to transform it to 'abdef'. The transformation requires that the character before the # symbol and the symbol itself (i.e. c and #) be removed from the from the string. Once this is done return the length of the transformed string. Use a stack to excute this task 
### Requirements:
1. Implement a `stringManipulation` function:
  ```cpp
  bool stringManipulation(string S, string T); // example declaration
  ```
  This function should return true if the strings matched else false.  
    **Example 1**
        * Input: S = "ab#c"
        * Output: 2
        * Explanation: S after processing becomes "ac" whose length is 2
    **Example 2**
        * Input: S = "ab##"
        * Output: 0
        * Explanation: S after processing becomes "" whose length in 0
    **Example 3**
        * Input: S = "a#bkb##c"
        * Output: 2
        * Explanation: S after processing becomes "bc".
2. The function stringManipulation has been defined in the driver.cpp file, you are required to complete it. You should use the stack operation from the stater code as and when required. Call it on all the above test case(as well as the ones you generate) and show that it works.
3. **Test your function** to make sure that it works in every case, no matter what list is passed in.
<div style="page-break-after: always;"></div>
Problem 3
----------
### Task:
In this assignment you will create a function that will append second array to the first one.
### Requirements
The function prototype is given as-
```cpp
void append(int* &arr1, int* &arr2, int size1, int size2)
```
where
* `arr1`: pointer to the first array
* `arr2`: pointer to the second array
* `size1`: size of the array1
* `size2`: size of the array2
*
__function will append array2 to array1__. So after calling the function elements of the array2 will be appended to array1. And size of array1 should become `size1 + size2`
You need to do the following as well-
* The main function will take size1 and size2 as command line arguments. Sample code for creating array1 is given in the starter code. You need to create the array2 in similar way. And then call the append function.
* After appending the arrays __do not forget to free up the memory space as required__.
* Print contents from the  array before and after append call. Each element should be separated by a `,`. There should not be any `,` after the last element.
# Example:
```
./a.out 5 3
arr1: 3,1,8,9,6
arr2: 5,7,12
arr1: 3,1,8,9,6,5,7,12
<div style="page-break-after: always;"></div>
