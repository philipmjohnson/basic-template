---
title: "Assignments"
published: true
morea_id: reading-assignments
morea_summary: "Requirements for programming assignments."
morea_type: reading
morea_sort_order: 6
---

Updated March 8, 2014 to discuss the use of GPL licenses.

This page discusses general procedures for implementation assignments and
extra credit projects. See the individual assignment pages for details.

## Implementation Assignments

### Overview

There will be three implementation assignments. These will involve writing
Java implementations of abstract data types and associated algorithms, and
testing the implementations on sample data. You will also provide instructions
on how to compile and run the program, document your design and implementation
(including complexith analysis), and present and discuss test results. The
assignments will progressively give you more responsibility. For the first
project, you will be told what to implement, and it will be weighted 6% (60
points). For the second assignment you will need to make some implementation
choices. The second assignment will be weighted 10% (100 points). The third
assignment will require some research and decision making on your part to
solve the problem. It will be weighted 10% (100 points).

### Software Requirements

The following requirements have been adopted from Dr. Sugihara:

#### Programming Language

All software must be written in Java. Other programming languages may not be
used except where specified by the assignment.

**The software must be compilable on the default version of Java available on uhunix.hawaii.edu** at the time of the submission deadline. The reason for this is to ensure that there is a common reference environment against which we can resolve disputes. We can't grade projects on claims that "it compiled on my machine".

Uhunix is running [Solaris](http://www.oracle.com/technetwork/server-
storage/solaris/overview/index.html). At this writing, the Java version is:

    
    
    java version "1.7.0_51"
    Java(TM) SE Runtime Environment (build 1.7.0_51-b13)
    Java HotSpot(TM) Server VM (build 24.51-b03, mixed mode)
    

Projects submitted with higher versions of Java (if they become available) are
at your risk. Note that the instructor is presently running research projects
in Java 1.6 in Snow Leopard on which Java 1.7 is not available. Some features
of Java 1.7 do not compile in 1.6, so if you could stick to 1.6 features he
won't have to go to UH Unix to run your code.

#### Program Type and Interface

The software should run as a Java application.

  * Command line (console) applications are acceptable.
  * GUI (graphical user interface versions) are also permissible.

#### Source Code Requirements

The student shall **submit .java source files** (not class or jar files),
organized in folders as required for your package structure, along with
instructions for compiling the program and other documentation discussed in
the next section.

  * The Teaching Assistant will verify that the programs compile on the current version of Java on uhunix, as specified above.
  * Submissions will only be evaluated for credit if they successfully compile.
  * This procedure is intended to (1) enable us to verify that the software is based on the student's own source code and (2) provide an objective basis for evaluating whether code works..

Source files should include the BSD License Header based on [ this
template,](../Resources/bsd_license_header.txt) with "<year>", "<copyright
holder>" and "<organization>" replaced appropriately.

Other open source licenses (e.g., [Apache](http://www.apache.org/licenses/) or
[GNU](http://www.gnu.org/licenses/)) may be used with prior permission from
the instructor if the student has a specific reason for doing so and
understands the consequences. See the discussion under Other Licenses two
sections below.

Source should include appropriate in-line comments documenting the software
design. Comments should not document the obvious (e.g., "this line adds 1 to
the index variable"), but rather document functional intent and constraints
such as loop invariants, explain something that would otherwise be obscure,
mark places that need improvement, etc. Descriptive use of variable and method
names also constitutes internal documentation. See next section for external
documentation requirements.

#### Including Open Source Software

Each assignment will specify where you are allowed to reuse source code of
open source software developed by other authors, and where you must write your
own code for the assignment. Where allowed by the assignment, reuse of open
source code is allowed if the following conditions are also met:

  * The software license of the reused open source code is compatible with the [ BSD license](http://www.opensource.org/licenses/bsd-license.php) (see discussion under Other Licenses below).
  * The license header of reused source code is also inserted into the source files containing the reused source code.
  * The `Readme.txt ` of your product clearly gives credit to the authors of the reused source code (i.e., including information such as the name of an author, the name of a reused product and a list of file names of the reused source code).

When source code of a module is reused, add the name(s) of its original
author(s) to an `@author` tag at the beginning of the reused module. If you
modified the source code for more than bug fixes, add your name as an author
of a derivative from the original source code:

>

>     /**

>      *

>      * @author     Original Author     James Brown

>      * @author     Derivative Author   Robert Smith

>      *

>      */

>  

#### Other Licenses

I am often asked whether one can use code under another license. You may use
other open source licenses as long as (1) they give you the right to use the
code under conditions acceptable to you and (2) you document this as needed.
An example is the GPL license. You may use a [GPL compatible
license](https://www.gnu.org/licenses/license-list.html), but you use this
license, all the code you write _must_ also be under GPL. See
<http://en.wikipedia.org/wiki/Free_software_license> for an overview, and read
some blogs about this hotly debated issue.

### Documentation Requirements

Software will be submitted with appropriate documentation, including the
following. (Think of your audience for this documentation as any potential
users, including your classmates as well as the TA and instructor.)

**Readme.txt (plaintext file)**
    Critical information that a user should know about your product first, including: 

  * step-wise instructions for the user to reconstruct an application from your source code (including the version of JDK used),
  * credits (acknowledgments to authors of open source reused at least in part for this product) including information such as the name of an author, the name of a reused product and a list of source file names of the reused product,
  * revision history (a log of changes on the product), 
  * bug report (description of known bugs), and 
  * a listing of other documentation available (below).
**Operation Manual (plaintext or PDF)**
    Concise, yet sufficient step-wise explanation about how to start and interact with the program, written for an end user who is concerned with using the program in an application domain (not with the code).
**Reference Manuals (plaintext or PDF, and Javadoc HTML)**
    Requirements and design specifications; organization of modules; algorithms and data structures used; functionality of each class or method; etc. A reference manual is written for experienced users and/or programmers who perform various maintenance activities for correction, enhancement, adaptation, etc. Javadoc pages may also be included, and should be included if you intend to have others use your code.
**Testing Document (plaintext or PDF)**
    Test plan describing objective(s) of testing, method(s) used for testing, assumption(s) of testing, and hardware/software environment in testing; test case specification describing classification of test cases; test data and I/O of test runs; and whatever else is useful to convince other people about the correctness and good features of your program. **For ICS 311 assignments the testing document will include your conclusions related to the purpose of the assignment.**

### Submission Requirements

  1. Place the files and folders required (as discussed above under Software and Documentation Requirements) in a folder titled using the scheme Last-First-A#, for example, Suthers-Dan-A1 for assignment 1, Suthers-Dan-A2 for assignment 2, etc. Extra credit projects should be submitted with extentions -E1, etc.
  2. Zip (.zip) or gzip (.gz) this folder using commands by those names on uhunix, or appropriate equivalents on your platform.
  3. It is suggested that you test unzipping, compiling and running the software per the instructions you gave before submitting the assignment.
  4. Upload the zip file to the Laulima area for the given assignment.
  5. You should receive email confirmation of your submission at the address registered in Laulima.
  6. Unlimited resubmissions are allowed up to the assignment deadline. Extra credit for early submission, if any, will be based on the date of the last submission, not the first!

### Evaluation Criteria for Implementation Assignments

### Warning: these will be revised for spring 2014

These are our default grading criteria. Some adjustments may be made when we
see where the greatest effort is required.

Program: 60%

    

  * 50% if all operations and all ADTs are implemented.
  * 5% for following instructions for input and output (although many more points will be deducted if the interface is so bad we can't verify that the operations and ADTs are implemented). 
  * 5% for adequate error handling. 
Analysis and Documentation 40%

    

  * 30% for adequate analysis of the results
  * 10% for Readme, Operation, Reference manuals

## Use of Software by Other Students

If others elect to use your software in a subsequent assignment (e.g., using
your graph ADT implementation in the third assignment), we will give extra
credit. See discussion in [Assessement](Assessment.html) page. Use should be
credited in the Readme and Reference Manual.

