Download Link: https://assignmentchef.com/product/solved-csc-115-fundamentals-of-programming-ii-assignment-5-the-emergency-room
<br>
Objectives: Upon completion of this assignment you need to be able to:

<ul>

 <li>Create a binary tree using an array.</li>

 <li>Create a version of the PriorityQueue ADT, using a Heap.</li>

 <li>Apply <em>data abstraction</em>, hiding a complex data type inside a simpler ADT.</li>

 <li>Experience the alternative to generics in Java, by casting the Object class.</li>

 <li>Continue to apply principles of inheritance, encapsulation and modularity.</li>

 <li>Continue to apply good programming practice in o designing programs o proper documentation, o testing and debugging problems with code.</li>

</ul>

______________________________________________________________________________

<strong>Resources:</strong>

<ul>

 <li>CSC 115 Java Coding Conventions.pdf (found on conneX, under Resources)</li>

 <li>Textbook Chapter 12</li>

 <li>The specification pages provided.</li>

</ul>

Introduction:

A group of patients are sitting in the local hospital’s Emergency waiting room, when the attending ER physician arrives for her shift.  The triage nurse has already assessed patients by their main complaint and provides an electronic device whereby the physician can touch the screen and the next patient chart is provided.  The order ing of the charts is determined by the patient’s priority and then time of check-in.  You have been selected to write part of the software that stores the patient information and prioritizes the list for the ER physician.  The project leader has elected to use a priority queue based on an array-based heap to store the ER_Patient objects.

Quick Start:

<ul>

 <li>If you haven’t done so already, download all the necessary documents for this assignment from conneX into a specific folder for CSC115 assignment five, assn5 is a recommended name. You may want to separate the documentation files into a separate directory.</li>

 <li>All of the specification documentation for public class and public methods can be found in the appropriate *.html</li>

 <li>The following classes are complete: java and NoSuchElementException.</li>

 <li>Familiarize yourself with the ER_Patient class, provided. Note that it implements</li>

</ul>

Comparable, but unlike the previous assignment, has no specific generic markings.

Because of this, the compareTo method takes an Object parameter and must make sure that the other Object is actually subclassed as a ER_Patient before doing the comparison.

<ul>

 <li>Complete the Heap Note that we are not using generics in this class and the warnings have been suppressed.  The Heap only handles objects of type Comparable. (Note that since an ER_Patient implements the Comparable interface, any object of type ER_Patient is by inheritance an object of type Comparable.)</li>

 <li>Complete the PriorityQueue class, noting that the Heap object is the main data field, and can handle most of the work the priority queue needs to do.</li>

</ul>

Detailed Instructions:

Chapter 12 of the textbook provides most of the background on the array-based heap and the PriorityQueue ADT.  Note that within the PriorityQueue, the Heap is completely hidden from the user, invoking the Information Hiding aspects of O-O programming.

<strong>Detailed steps to completing the Heap</strong><strong> class:</strong>

<ol>

 <li>The shell is provided for this class. Fill in the comments above each of the public methods and write the code that makes these methods work.</li>

 <li>Add additional data fields as necessary. Add additional private methods that help maintain both the structure and ordering of the Heap array during inserts and removals. A private print out of the array is always recommended, as are separate methods for <em>bubbling</em> an item upwards or downwards.</li>

 <li>You must not change the provided method headers or the given data fields. There are two reasons for this requirement:

  <ol>

   <li>You are a programmer on a team; others are expecting their code to plug into your code.</li>

   <li>You are a student in CSC115, doing an exercise that enhances your skills as a programmer. To obtain adequate feedback, the marker(s) are counting on easy access to your implementation.</li>

  </ol></li>

 <li>Note that the array size is not determined or limited. Somewhere in the source code, there must be a provision for increasing the size of the array to accommodate large numbers of items. Create a private method that doubles the size of the array to accommodate more items into a full array.</li>

 <li>You must test every method internally. The more rigorously you test, the more robust your code. Do not move to the next step until you are confident that the Heap works as expected.</li>

</ol>

◦ Note that the ER_Patient internal class uses Thread.sleep() to spread a single second between admit times.  You may use this technique or choose the constructor to create your own admit times.  <em>For the sake of the marker’s sanity, DO NOT use </em>Thread.sleep<em> in any method other than main.</em>

<strong>Detailed steps to completing the PriorityQueue class:</strong>

<ol>

 <li>The shell is provided for this class. Fill in the comments above each of the public methods and write the code that makes these methods work.</li>

 <li>Let the hidden Heap data structure do all the work in each of the PriorityQueue</li>

 <li>Test the PriorityQueue. If the Heap has been thoroughly tested, it is sufficient to insert a few patients and then dequeue and print until the queue is empty. A sorted print out indicates success.</li>

</ol>

<strong>A note about the Heap vs. the PriorityQueue:</strong>

A PriorityQueue can use a linked data structure, an un-ordered array, an ordered array, or a tree as its underlying data structure.  We use the Heap in this exercise, because the Heap data structure is so beautifully similar to the PriorityQueue and takes O(log n) for both insert and remove operations.  However, the Heap is a complete binary tree data structure and is not necessarily bound by the PriorityQueue ADT.  For instance, it is allowed to have an iterator and it is allowed to have a size method.  There are other tree-related methods such as isInternal that are not part of the PriorityQueue ADT.  There is also nothing stopping a Heap from deleting an item in the middle of its structure, although there are better data structures for that kind of operation.

The PriorityQueue ADT is much more limiting.  For that reason, you want to make sure that the user does not ever have access to the Heap itself.  It is desirable to have the PriorityQueue hide any extra functionality of the Heap.

Submission

Submit the following completed files to the Assignment folder on conneX:

<ul>

 <li>java</li>

 <li>java</li>

</ul>

Please make sure that conneX has sent you a confirmation email.  Do not send [.class] (the byte code) file, or any another file for this assignment.  Also make sure you <em>submit</em> your assignment, not just save a draft.  All draft copies are not available to the instructors, so we cannot mark them.