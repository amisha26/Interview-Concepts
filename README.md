
## <a name='toc'>Table of Contents</a>
 * [Arrays](#Arrays)
 * [Backtracking](#Backtracking)
 * [Big-O Notation](#Big-ONotation)
 * [Binary Tree](#BinaryTree)
 * [Bit Manipulation](#BitManipulation)
 * [Brain Teasers](#BrainTeasers)
 * [Divide & Conquer](#Divide&Conquer)
 * [Dynamic Programming](#DynamicProgramming)
 * [Fibonacci Series](#FibonacciSeries)
 * [Graph Theory](#GraphTheory)
 * [Greedy Algorithms](#GreedyAlgorithms)
 * [Hash Tables](#HashTables)
 * [Heaps and Maps](#HeapsandMaps)
 * [Linked Lists](#LinkedLists)
 * [Queues](#Queues)
 * [Recursion](#Recursion)
 * [Searching](#Searching)
 * [Sorting](#Sorting)
 * [Stacks](#Stacks)
 * [Strings](#Strings)
 * [Trees](#Trees)
 * [Trie](#Trie)
## [[⬆]](#toc) <a name=Arrays>Arrays</a> Interview Questions
#### Q1: Explain what is an Array? ⭐
**Answer:**
An **array** is a collection of **homogeneous** (same type) data items stored in **contiguous memory** locations. For example if an array is of type “int”, it can only store integer elements and cannot allow the elements of other types such as double, float, char etc. The elements of an array are accessed by using an **index**. 

* <code><i>O</i>(<i>1</i>)</code>
* <code><i>O</i>(<i>log n</i>)</code>
* <code><i>O</i>(<i>n</i>)</code>
* <code><i>O</i>(<i>n log n</i>)</code>
* <code><i>O</i>(<i>n</i><sup>2</sup>)</code>
* <code><i>O</i>(<i>2</i><sup>n</sup>)</code>
* <code><i>O</i>(<i>n!</i>)</code>



#### Q2: Name some characteristics of Array Data Structure ⭐
**Answer:**
Arrays are: 
* **Finite (fixed-size)** - An array is finite because it contains only limited number of elements.
* **Order** -All the elements are stored one by one , in contiguous  location of computer memory in a linear order and fashion
* **Homogenous** - All  the elements of an array are of  same  data types only  and hence  it is termed as collection of homogenous



#### Q3: Name some advantages and disadvantages of Arrays ⭐⭐
**Answer:**
**Pros:**
* **Fast lookups**. Retrieving the element at a given index takes `O(1)` time, regardless of the length of the array.
* **Fast appends**. Adding a new element at the end of the array takes `O(1)` time.

**Cons:**
* **Fixed size**. You need to specify how many elements you're going to store in your array ahead of time.
* **Costly inserts and deletes**. You have to shift the other elements to fill in or close gaps, which takes worst-case `O(n)` time.



#### Q4: What is time complexity of basic Array operations? ⭐⭐
**Answer:**
Array uses continuous memory locations (**space** complexity `O(n)`) to store the element so **retrieving** of any element will take `O(1)` time complexity (constant time by using index of the retrieved element). `O(1)` describes **inserting** at the end of the array. However, if you're inserting into the middle of an array, you have to shift all the elements after that element, so the complexity for insertion in that case is `O(n)` for arrays. End appending also discounts the case where you'd have to resize an array if it's full.


|Operation	|Average Case	|Worst Case
|-|-|-|
|Read	    | `O(1)`	        |`O(1)`
|Append       |`O(1)`            |`O(1)`
|Insert	   |`O(n)`	        |`O(n)`
|Delete	   |`O(n)`	        |`O(n)`
|Search	   |`O(n)`	        |`O(n)`




#### Q5: What is a main difference between an Array and a Dictionary? ⭐⭐
**Answer:**
Arrays and dictionaries both store collections of data, but differ by _how they are accessed_. Arrays provide _random access_ of a sequential set of data. Dictionaries (or associative arrays) provide a _map_ from a _set of keys_ to a _set of values_. 
* Arrays store a set of objects (that can be accessed randomly)
* Dictionaries store pairs of objects
* Items in an array are accessed by position (_index_) (often a number) and hence have an order. 
* Items in a dictionary are accessed by _key_ and are unordered.

This makes array/lists more suitable when you have a group of objects in a set (prime numbers, colors, students, etc.). Dictionaries are better suited for showing relationships between a pair of objects.



#### Q6: What are Dynamic Arrays? ⭐⭐
**Answer:**
A **dynamic array** is an array with a big improvement: _automatic resizing_.

One limitation of arrays is that they're _fixed_ size, meaning you need to specify the number of elements your array will hold ahead of time. A dynamic array expands as you add more elements. So you don't need to determine the size ahead of time.


#### Q7: How do Dynamic Arrays work? ⭐⭐
**Answer:**
A simple dynamic array can be constructed by _allocating an array of fixed-size_, typically _larger_ than the number of elements immediately required. The elements of the dynamic array are stored contiguously at the start of the underlying array, and the remaining positions towards the end of the underlying array are reserved, or unused. Elements can be added at the end of a dynamic array in constant time by using the reserved space until this space is completely consumed.

When all space is consumed, and an additional element is to be added, the underlying fixed-sized array needs to be increased in size. Typically resizing is expensive because you have to allocate a bigger array and copy over all of the elements from the array you have overgrow before we can finally append our item.

Dynamic arrays memory allocation is language specific. For example in C++ arrays are created on the stack, and have automatic storage duration -- you don't need to manually manage memory, but they get destroyed when the function they're in ends. They necessarily have a fixed size:

```js
int foo[10];
```

Arrays created with operator `new[]` have _dynamic_ storage duration and are stored on the heap (technically the "free store"). They can have any size, but you need to allocate and free them yourself since they're not part of the stack frame:

```js
int* foo = new int[10];
delete[] foo;
```


**Important Questions:**

#### Q8: What is an Associative Array? 

#### Q9: What are time complexities of sorted array operations? 

#### Q10: What does Sparse Array mean? 

#### Q11: When to use a Linked List over an Array/Array List? 

#### Q12: Compare Array based vs Linked List stack implementations 

#### Q13: How exactly indexing works in Arrays? 

#### Q14: What are advantages of Sorted Arrays? 

#### Q15: What is the advantage of Heaps over Sorted Arrays? 

#### Q16: How to merge two sorted Arrays into a Sorted Array? 

#### Q17: What defines the dimensionality of an Array? 

#### Q18: How would you compare Dynamic Arrays with Linked Lists and vice versa? 

#### Q19: Why is the complexity of fetching from an Array be <code><i>O</i>(<i>1</i>)</code>?

#### Q20: How to implement 3 Stacks with one Array? 

#### Q21: Check for balanced parentheses in linear time using constant space 

<hr>

## [[⬆]](#toc) <a name=Backtracking>Backtracking</a> Interview Questions


#### Q1: What is Backtracking? ⭐
**Answer:**
**Backtracking** is a systematic way of trying out different sequences of decisions until we find one that "works." Backtracking does not generate all possible solutions first and checks later. It tries to generate a solution and as soon as even one constraint fails, the solution is rejected and the next solution is tried.

Backtracking can be understood as as searching os a tree for a particular "goal" leaf node. Backtracking in that case is a **depth-first search** with any bounding function. All solution using backtracking is needed to satisfy a complex set of constraints.


![](https://static.javatpoint.com/tutorial/daa/images/backtracking-introduction.png)



#### Q2: What is the difference between Backtracking and Recursion? ⭐⭐
**Answer:**
* **Recursion** describes the calling of the _same function_ that you are in. The typical example of a recursive function is the factorial. You always need a condition that makes recursion stop (base case). 
* **Backtracking** is when the algorithm makes an opportunistic decision<sup>*</sup>, which may come up to be wrong. If the decision was wrong then the backtracking algorithm restores the state before the decision. It builds candidates for the solution and abandons those which cannot fulfill the conditions. A typical example for a task to solve would be the _Eight Queens Puzzle_. Backtracking is also commonly used within _Neuronal Networks_. Many times backtracking is not implemented recursively. If backtracking uses recursion its called **Recursive Backtracking**

P.S. <sup>*</sup> **Opportunistic decision** making refers to a process where a person or group assesses alternative actions made possible by the favorable convergence of immediate circumstances recognized **without** reference to any **general plan**.



#### Q3: Why is this called Backtracking? ⭐⭐
**Answer:**
1. Using Backtracking you built a **solution** (that is a structure where every variable is assigned a value).
2. It is however possible that during construction, you realize that the solution is **not successful** (does not satisfy certain constraints), then you **backtrack**: you _undo_ certain assignments of values to variables in order to reassign them.

Like when looking for a book  because at first you check drawers in the first room, but it's not found, so you _backtrack_ out of the first room to check the drawers in the next room. It's also called **Trial & Error**.


#### Q4: What is Exhaustive Search? ⭐⭐
**Answer:**
**Exhaustive Search** is an algorithmic technique in which first all possible solutions are generated first and then we select the most feasible solution by applying some rules. Since it follows the most naive approach, it is a.k.a **Brute-Force Search**. This approach is one of the **most expensive** algorithmic techniques, mainly in terms of time complexity. It is also, therefore, one of the most **naive** ones.

#### Q5: Explain what is DFS (Depth First Search) algorithm for a Graph and how does it work? 


#### Q6: Find all the Permutations of a String 


#### Q7: What is the difference between Backtracking and Exhaustive Search techniques? 


#### Q8: Explain what is Explicit and Implicit Backtracking Constrains? ⭐

<hr>


## [[⬆]](#toc) <a name=Big-ONotation>Big-O Notation</a> Interview Questions
#### Q1: What is _Big O_ notation? ⭐
**Answer:**
**Big-O** notation (also called "asymptotic growth" notation) is a relative representation of the complexity of an algorithm. It shows how an algorithm *scales* based on input size. We use it to talk about how thing _scale_. Big O complexity can be visualized with this graph:


![](https://i.stack.imgur.com/WcBRI.png)



#### Q2: Provide an example of <code><i>O</i>(<i>1</i>)</code> algorithm ⭐
**Answer:**
Say we have an array of `n` elements:

```cs
int array[n];
```

If we wanted to access the first (or any) element of the array this would be <code><i>O</i>(<i>1</i>)</code> since it doesn't matter how big the array is, it always takes the same constant time to get the first item:
```cs
x = array[0];
```


#### Q3: What is Worst Case? ⭐⭐
**Answer:**
Big-O is often used to make statements about functions that measure the worst case behavior of an algorithm. **Worst case** analysis gives the maximum number of basic operations that have to be performed during execution of the algorithm. It assumes that the input is in the _worst possible state_ and maximum work has to be done to put things right.


#### Q4: What the heck does it mean if an operation is <code><i>O</i>(<i>log n</i>)</code>? ⭐⭐
**Answer:**
**<code><i>O</i>(<i>log n</i>)</code>** means for every element, you're doing something that only needs to look at **log N** of the elements. This is usually because you know something about the elements that let you make an _efficient choice_ (for example to reduce a _search space_). 
The most common attributes of logarithmic running\-time function are that:
*   the choice of the next element on which to perform some action is one of several possibilities, and
*   only one will need to be chosen

or

*   the elements on which the action is performed are digits of `n`

Most efficient sorts are an example of this, such as **merge sort**. ​It is `O(log n)` when we do divide and conquer type of algorithms e.g binary search. Another example is **quick sort** where each time we divide the array into two parts and each time it takes `O(N)` time to find a pivot element. Hence it `N O(log N)`

Plotting `log(n)` on a plain piece of paper, will result in a graph where the rise of the curve decelerates as `n` increases:
![](https://i.stack.imgur.com/qPNNp.png)



#### Q5: Why do we use Big O notation to compare algorithms?  ⭐⭐
**Answer:**
The fact is it's difficult to determine the exact runtime of an algorithm. It depends on the speed of the computer processor. So instead of talking about the runtime directly, we use Big O Notation to talk about _how quickly the runtime grows_ depending on input size.

With Big O Notation, we use the size of the input, which we call `n`. So we can say things like the runtime grows “on the order of the size of the input” (<code><i>O</i>(<i>n</i>)</code>) or “on the order of the square of the size of the input” (<code><i>O</i>(<i>n</i><sup>2</sup>)</code>). Our algorithm may have steps that seem expensive when `n` is small but are eclipsed eventually by other steps as `n` gets larger. For Big O Notation analysis, we care more about the stuff that grows fastest as the input grows, because everything else is quickly eclipsed as `n` gets very large.


#### Q6: What exactly would an <code><i>O</i>(<i>n</i><sup>2</sup>)</code> operation do? ⭐⭐
**Answer:**
**<code><i>O</i>(<i>n</i><sup>2</sup>)</code>** means for every element, you're doing something with _every_ other element, such as comparing them. Bubble sort is an example of this.


#### Q7: What is complexity of this code snippet? ⭐⭐
**Details:**
Let's say we wanted to find a number in the list:
```js
for (int i = 0; i < n; i++){
    if(array[i] == numToFind){ return i; }
}
```
What will be the time complexity (Big O) of that code snippet?

**Answer:**
This would be <code><i>O</i>(<i>n</i>)</code> since at most we would have to look through the entire list to find our number. The Big-O is still <code><i>O</i>(<i>n</i>)</code> even though we might find our number the first try and run through the loop once because Big-O describes the upper bound for an algorithm.


#### Q8: What is complexity of `push` and `pop` for a Stack implemented using a LinkedList? ⭐⭐
**Answer:**
<code><i>O</i>(<i>1</i>)</code>. Note, you don't have to insert at the end of the list. If you insert at the front of a (singly-linked) list, they are both `O(1)`.

Stack contains 1,2,3:

```py
[1]->[2]->[3]
```

Push 5:

```js
[5]->[1]->[2]->[3]
```

Pop:

```js
[1]->[2]->[3] // returning 5
```


#### Q9: Explain the difference between _`O(1)`_ vs _`O(n)`_ space complexities  ⭐⭐
**Answer:**
Let's consider a traversal algorithm for traversing a list.

* <code><i>O</i>(<i>1</i>)</code> denotes _constant_ space use: the algorithm allocates the same number of pointers irrespective to the list size. That will happen if we move (reuse) our pointer along the list.
* In contrast, <code><i>O</i>(<i>n</i>)</code> denotes _linear_ space use: the algorithm space use grows together with respect to the input size `n`. That will happen if let's say for some reason the algorithm needs to allocate 'N' pointers (or other variables) when traversing a list.


#### Q10: What is an algorithm? 

#### Q11: What is complexity of this code snippet? 

#### Q12: What is the time complexity for "Hello, World" function? 

#### Q13: What is meant by "Constant Amortized Time" when talking about time complexity of an algorithm? 

#### Q14: Why do we use Big O instead of Big Theta (Θ)? 

#### Q15: Name some types of Big O complexity and corresponding algorithms 

#### Q16: What is complexity of "Reading a Book"? 

#### Q17: Explain your understanding of "Space Complexity" with examples 

#### Q18: What is the difference between Lower bound and Tight bound? 

#### Q19: What does it mean if an operation is <code><i>O</i>(<i>n!</i>)</code>? 

#### Q20: Provide an example of algorithm with time complexity of <code><i>O</i>(<i>c</i><sup>k</sup>)</code>? 

#### Q21: What are some algorithms which we use daily that has _`O(1)`_, _`O(n log n)`_ and _`O(log n)`_ complexities? 

#### Q22: What is the big O notation of this function? 

<hr>


## [[⬆]](#toc) <a name=BinaryTree>Binary Tree</a> Interview Questions
#### Q1: Define Binary Tree ⭐
**Answer:**
A normal tree has no restrictions on the number of children each node can have. A **binary tree** is made of nodes, where each node contains a "left" pointer, a "right" pointer, and a data element. 

There are three different types of binary trees:

* **Full binary tree**: Every node other than leaf nodes has 2 child nodes.
* **Complete binary tree**: All levels are filled except possibly the last one, and all nodes are filled in as far left as possible.
* **Perfect binary tree**: All nodes have two children and all leaves are at the same level.



![](https://study.com/cimages/multimages/16/0e0646ba-30e5-40d9-b45c-a138f038f05b_full_complete_perfect.png)



#### Q2: What is Binary Search Tree? ⭐⭐
**Answer:**
**Binary search tree** is a data structure that quickly allows to maintain a _sorted list_ of numbers.

* It is called a _binary tree_ because each tree node has maximum of two children.
* It is called a _search tree_ because it can be used to search for the presence of a number in `O(log n)` time.

The properties that separates a binary search tree from a regular binary tree are:

* All nodes of left subtree are less than root node
* All nodes of right subtree are more than root node
* Both subtrees of each node are also BSTs i.e. they have the above two properties


![](https://cdn.programiz.com/sites/tutorial2program/files/bst-vs-not-bst.jpg)



#### Q3: Explain the difference between Binary Tree and Binary Search Tree with an example? 

#### Q4: Why do we want to use Binary Search Tree? 

#### Q5: What is AVL Tree? 

#### Q6: What are advantages and disadvantages of BST? 

#### Q7: What is Balanced Tree and why is that important? 

#### Q8: Convert a Binary Tree to a Doubly Linked List 

#### Q9: What is the difference between Heap and Red-Black Tree? ⭐

#### Q10: Explain how to balance AVL Tree? ⭐

#### Q11: How does inserting or deleting nodes affect a Red-Black tree? ⭐

#### Q12:  Explain what the main differences between red-black (RB) trees and AVL trees ⭐

#### Q13: What is Red-Black tree? ⭐

#### Q14: Build a Binary Expression Tree for this expression ⭐

#### Q15: What is the time complexity for insert into Red-Black Tree? ⭐

#### Q16: Is there any reason anyone should use BSTs instead of AVLs in the first place? ⭐

#### Q17: What are main advantages of Tries over Binary Search Trees (BSTs)? ⭐

#### Q18: What's the main reason for choosing Red Black (RB) trees instead of AVL trees? ⭐⭐

#### Q19: How is an AVL tree different from a B-tree? ⭐⭐

<hr>