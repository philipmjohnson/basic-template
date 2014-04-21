---
title: "Battle of the Dynamic Sets"
published: true
morea_id: experience-project-1
morea_type: experience
morea_summary: "Provide four implementations of the Dynamic Set ADT and compare their performance."
morea_sort_order: 1
morea_labels:
 - Programming
---

# Battle of the Dynamic Sets

Late submissions with **penalty of 1% per hour** accepted until 2AM Saturday
March 15th, at which time the deduction reaches 50%. (If you used all that
time and turned in a perfect "A+" project, you would get a "C".)


### Change Log

Mar 10, 2014

    Assignment extended three days. Corrected the late deadline on March 11th.
Mar 1, 2014

    Changed the interface to Robert Ward's version with generics and comparable.
Feb 7, 2014

    Added delete to operations to be tested. 
Feb 6, 2014

    First released version. This differs from the 2012 and 2013 versions. 

## Overview

You will provide four implementations of the Dynamic Set ADT (see below,
modified from [Topic 4 Notes](/morea/040.adt/reading-notes-4.html)). You will then analyze their expected
performance (this has been largely done in the lectures and textbook), and
then test them empirically to see how your test data compares to expected
performance. You will write a report on the results. The project is worth 60
points.

You may either use open source implementations of the following data
structures (see the [Assignments Page](/morea/010.introduction/reading-assignments.html) Section "Including Open Source Software"
for requirements), or implement them yourself:

  * **Sorted Doubly Linked Lists** (Chapter 10 or [Notes/Topic-04](morea/040.adt/reading-notes-4.html)) 
  * **Skip Lists** ([Notes/Topic-05](morea/050.probabilistic/reading-notes-5.html) or ftp://ftp.cs.umd.edu/pub/skipLists/skiplists.pdf) 
  * **Binary Search Trees** (Chapter 12 or [ Notes/Topic-08](morea/080.binary-search-trees/reading-notes-8.html)) 
  * **Red-Black trees** (Chapter 13 or [Notes/Topic-11]morea/110.balanced-trees/reading-notes-11.html)): for this, use Java TreeMap. 

There are several advantages to implementing at least some of these
yourself:

  * Others' implementations may have incompatible assumptions.
  * You will understand the data structures and algorithms better
  * You can then offer your implementation to other students for extra credit in Implementation Project 2.

You will then write your own code, including:

  * Implementations of Dynamic Sets that use these data structures;
  * A main method to read in a file of strings, insert these in the dynamic set as keys, and run tests on all four implementations as specified below.

We will provide you with data in the form of files of keywords (automatically
generated names). There will be ten data files, three _unsorted_ and three
_sorted_ of size 100, 1000, 10,000, 100,000 and 1,000,000. (See discussion
below concerning the largest file.) We may use other data files in our
testing, so make your code robust!

Your accompanying report will provide the **minimum**, **average** and
**maximum** times in **nanoseconds** required for: `insert`, `retrieve`,
`successor`, and `predecessor`, and the actual time for `minimum` and
`maximum`, for each of the input files. You will compare these results to the
theoretical analyses for the algorithms. While `delete` is not included in the
timing tests, we will test that deletion works.

Details follow. Questions and requests for clarification are welcome and
should be submitted early.

## Dynamic Set ADT

Note that this **ADT has been changed**: it is not the same as the one in the
lecture notes, and it is not the same as the ones used in my 2012 or 2013
classes. Also, it was changed to use generics.

{% highlight java linenos %}
    package ics311;
    import java.util.Map.Entry;

    
    /**
     * This interface is to be used for all of the Dynamic Sets you create for this assignment.
     * 
     * @author      Robert Ward
     * @version     1.0       
     * @since       2014-02-01
     */
    public interface DynamicSet<Key extends Comparable<Key> , Value> {
        
       /**
        * Returns the name of Data Structure this set uses. 
        *           
        * @return  the name of Data Structure this set uses. 
        */
        public String setDataStructure();

       /**
        * Returns the number of key-value mappings in this set. 
        * This method returns zero if the set is empty
        *           
        * @return  the number of key-value mappings in this set. 
        */
        public int size();
       
       /**
        * Associates the specified value with the specified key in this map.
        * If the map previously contained a mapping for the key, the old value is replaced. 
        * If there is no current mapping for this key return null,
        * otherwise the previous value associated with key. 
        * 
        * @param  key - key with which the specified value is to be associated
        * @param  value - value to be associated with the specified key
        * 
        * @return the previous value associated with key, or null if there was no mapping for key. 
        *  (A null return can also indicate that the map previously associated null with key.)  
        */
        public Value insert(Key key, Value value);
        
       /**
        * Removes the mapping for this key from this set if present.
        *
        * @param key - key for which mapping should be removed
        * 
        * @return the previous value associated with key, or null if there was no mapping for key. 
        * (A null return can also indicate that the map previously associated null with key.) 
        */
        public Value delete(Key key);
      
    
       /**
        * Returns the value to which the specified key is mapped, or null if this set contains no
        * mapping for the key. 
        * 
        * @param  key The key under which this data is stored. 
        *   
        * @return the Value of element stored in the set under the Key key.
        */
        public Value retrieve(Key key);
       
       
       /**
        * Returns a key-value mapping associated with the least key in this map, or null if the set
        * is empty. 
        * IMPORTANT: This operation only applies when there is a total ordering on the Key 
        * Returns null if the set is empty. If there is not total ordering on the Key returns null.  
        * 
        * @return an entry with the least key, or null if this map is empty
        */
        public Entry<Key, Value>  minimum( );
       
    
       /**
        * Returns a key-value mapping associated with the greatest key in this map, or null if the
        * map is empty. 
        * IMPORTANT: This operation only applies when there is a total ordering on the Key 
        * Returns null if the set is empty. If there is not total ordering on the key returns null. 
        * 
        * @return an entry with the greatest key, or null if this map is empty.
        */
        public Entry<Key, Value>  maximum( );
       
        
       /**
        * Returns a key-value mapping associated with the least key strictly greater than the given
        * key, or null if there is no such key. 
        * IMPORTANT: This operation only applies when there is a total ordering on the key 
        * Returns null if the set is empty or the key is not found. 
        * Returns null if the key is the maximum element. 
        * If there is not total ordering on the key for the set returns null. 
        * @param key - the key
        * 
        * @return an entry with the greatest key less than key, or null if there is no such key
        */
        public Entry<Key, Value>  successor(Key key);
        
       /**
        * Returns a key-value mapping associated with the greatest key strictly less than the given
        * key, or null if there is no such key. 
        * IMPORTANT: This operation only applies when there is a total ordering on the key 
        * Returns null if the set is empty or the key is not found. 
        * Returns null if the key is the minimum element. 
        * If there is not total ordering on the key for the set returns null. 
        * @param key - the key
        * 
        * @return an entry with the greatest key less than key, or null if there is no such key
        */
        public Entry<Key, Value>  predecessor(Key key);
    
    }
{% endhighlight %}

### Comments on ADT

If you wish, to simplify things you may change KeyType to String. The data
`Object d` stored under a key is not important for our testing: just give it
the key `k`.

In a real implementation, returning a key in `minimum`, `maximum`, `successor`
and `predecessor` would be inefficient if the client then has to use
`retrieve` to get the data. This could be solved by using the position
abstraction, or by returning multiple values (key + data). But for our
purposes we only need the key to test runtime.

### Implementing the ADT

You will have four classes implementing this interface, named to reflect the
implementation:

  * **`DLLDynamicSet`**: Doubly Linked List implementation, using OSS 
  * **`SkipListDynamicSet`**: Skip List implementation, using OSS
  * **`BSTDynamicSet`**: Binary Search Tree implementation, using OSS
  * **`RedBlackDynamicSet`**: Red Black Tree implementation, _using Java TreeMap_

To implement the ADT you need to write the methods that are specified by the
interface but map to the underlying implementation. As a simple example, in
RedBlackDynamicSet the interface method   `retrieve (KeyType k)` will be
implemented by calling TreeMap's `get(Object key)`. This is trivial code, but
it accomplishes an important objective: hiding the details of the
implementation behind the interface.

We suggest that you implement **`RedBlackDynamicSet`** first and get the rest
of the program running on it, as you already have this implementation. Then
either write or look for OSS of the other three and add them to the testing.

In general, you are free to make your own implementation decisions and use the
best practices you are capable of. This includes whether or not you use
Comparable or generics, whether you use locator abstractions (such as Goodrich
& Tamassia's "position") rather than returning pointers to data stored, how
much error checking is done, etc. The important thing is that you have
implemented the set operations in a general way, and in particular can run the
tests.

We suggest that you organize your code in packages, but this is not required.

* * *

## Test Data

Files including from 100 to 1,000,000 keys, sorted and unsorted, are available
in [this directory](http://www2.hawaii.edu/~suthers/courses/ics311s14/Projects
/Project-1/). Each file has one name on each line. There are no quotations or
other delimiters other than newline. For example:
    
    Hugh Moreno 
    Traci Obrien 
    Doug Moore 
    Sammy West 
    Anne Reid 
    Deanna Zimmerman 
    Marcus Waters 
    Clyde Walton 
    Matthew Rios 
    Jacqueline Robertson
    ...
    

Your program will take the input file name as an argument at the command line
(i.e., read into String args). It will read the file into an array until end
of file is reached. We need to read into an array because we will be randomly
selecting elements for test runs. You do not need to test the input for any
properties: just read each line from the file as if it is a string.

* * *

## Input

Your program will read an argument from the command line: the name of the file
to be loaded in this test run.

Read the string keys in the specified file into an array. Count the keys as
you read them so you know what your _n_ is. You will then use this array to
drive a test of each of the Dynamic Set implementations, as discused in the
next section.  

Screencasts are available showing how to read in data from a file if you have
forgotten.

* * *

## Tests

Each `runtest` run will use `System.nanoTime()` (we have found that
`System.currentTimeMillis()` is not precise enough for O(lg n) algorithms) to
time the following operations and report **minimum**, **average** and
**maximum** times required:

  * `insert(k):` min, avg and max across all keys. (You have all the keys in the array. Insert all of them into the data structure, timing the time it takes for each insertion and keeping track of min, max and sum of times as you go so you can compute average at the end.) 
  

  * `retrieve(k):` Use the `Random` class to produce 10 integers in the range of the data array. Then search for the 10 keys (name strings) indexed by these random numbers, timing each search. Report min, avg and max across these 10 searches.
  

  * `successor(k):` run 10 trials on the same keys you used in the above retrieval tests. Report min, avg and max. 
  

  * `predecessor(k):` run 10 trials on the same keys you used in the above retrieval tests. Report min, avg and max.
  

  * `minimum:` Report time to run one call (since there is only one minimum). 
  

  * `maximum:` Report time to run one call (since there is only one maximum). 
  

  * `delete(k):` Last, delete the 10 randomly chosen keys you used above, timing the deletion. Report min, avg and max.
  

(_Note: _ 10 has been specified as the number of trials because the smallest
data set has only 100 elements. 10 trials will give you meaningful results,
but in real world testing you'd run many more trials for more reliable and
convincing averages. Compared to the cost of programming this test, computer
trials are cheap! One approach is to use a percentage, e.g., 10% of the keys
would give you 100 trials on the data set of 1000.)

#### Memory:

If you run out of memory, increase the heap size available to Java using the
-Xmx argument (or set the corresponding preference in your IDE). Try 1024M, or
higher if you have the disk space to spare. (For one of my Java-based research
projects, I set this value to 32G, which is _twice_ the physical memory on my
16G machine: Java will use virtual memory.)

Also try loading the data directly into one Dynamic Set implementation at a
time (skipping the array and the interactive interface), and then destroying
all references to each dynamic set after you test it so it can be garbage
collected before loading into the next one from the file.

If you are unable to run the test file of one million, turn in up to 100,000
along with an explanation.


## Output

Each `runtest` run will generate an output table as follows (this layout is
designed to enable you to print the table out incrementally as you go).

    
    
    Size: N
    --------------------------------------------------------------------------------------
                | Insert   | Retrieve | Pred     | Succ     | Min    | Max    | Delete   |
    --------------------------------------------------------------------------------------
    Linked List |          |          |          |          |        |        |          |  
    --------------------------------------------------------------------------------------
    Skip List   |          |          |          |          |        |        |          |
    --------------------------------------------------------------------------------------
    Binary Tree |          |          |          |          |        |        |          |
    --------------------------------------------------------------------------------------
    RB Tree     |          |          |          |          |        |        |          |
    --------------------------------------------------------------------------------------
    

The entry in each cell of this table will be of form

    
    
             -------------------
             | min / avg / max |
             -------------------
    

(except `minimum` and `maximum`), each being in nanoseconds. (Resize the table
as needed to fit.)

You will need to run the program once for each data set: 100, 1000, 10,000,
100,0000, and, if possible, 1,000,000; each sorted and unsorted. Thus you will
have at least 8 runs (8 tables) if you go up to 100,000, or 10 runs (10
tables) if you are able to include the 1,000,000. Your reports will be based
on these tests, in comparison to the Θ, big-O, and Ω analyses for the
algorithms.

The TA may use other data sets, which may include reverse sorted items,
duplicates, etc.

* * *

## Documentation and Report

Requirements stated on the [ Assignments Page](/morea/010.introduction/reading-assignments.html) are included in the requirements
for this project. Read that first. Further comments are below.

###  Readme.txt

The Readme file should be clear and enable the TA to compile and run your
program.

### Operation and Reference Manuals

For this assignment, the Operation manual is not required _ as long as you put
the instructions on how to run the program in your Readme.txt._ The Reference
manual can be brief, as the program as a whole is not intended to be
distributed for general use. Describe the organization of your program and the
source of the implemenatations: anything that you as a programmer maintaining
the code would want to know.

### Testing Document (30% of grade)

The Testing Document will include a summary of your empirical test results and
a discussion of how these results compare to the asymptotic analyses of the
underlying data structures.

Put the tables output by your program in the appendix of your testing
document. Then, in the beginning of your testing document discuss whether the
times you got fit the theoretical analyses for the various data structures.
Did implementations behave as expected as _n_ gets bigger? Does the different
between sorted and unsorted data make sense? How do they compare to each
other?

**This document is 30% of your grade:** be thorough (showing you have thought carefully about the results in relation to the theoretical analyses and your implementation), yet concise (don't put in a lot of blather to make it look bigger). 

* * *

## Grading

### Program: 60%

  * 5% for correct handling of input as specified. This includes reading command line arguments and error handling. 
  * 40% = 10% x 4 for each correct implementation of the Dynamic Set ADT. 
  * 10% for proper organization of the tests (reading data into array; running one ADT at a time and recording values; able to run up to one million). 
  * 5% for providing output table as specified. 

### Analysis and Documentation: 40%

  * 30% for adequate analysis of the results (in the Testing Document)
  * 10% for Readme and Reference manuals

* * *

Dan Suthers Last modified: Tue Mar 11 03:27:03 HST 2014

