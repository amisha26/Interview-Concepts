
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
