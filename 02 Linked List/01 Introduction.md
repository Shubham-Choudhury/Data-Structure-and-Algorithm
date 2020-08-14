A linked list is a linear data structure, in which the elements are not stored at contiguous memory locations. The elements in a linked list are linked using pointers as shown in the below image:

<img src="/Source Images/Linkedlist.png" alt="Linked List">

In simple words, a linked list consists of nodes where each node contains a data field and a reference(link) to the next node in the list.

- **ADVANTAGES OF LINKED LIST:**

   1. Linked List is Dynamic data Structure .
   2. Linked List can grow and shrink during run time.
   3. Insertion and Deletion Operations are Easier
   4. Efficient Memory Utilization ,i.e no need to pre-allocate memory
   5. Faster Access time,can be expanded in constant time without memory overhead
   6. Linear Data Structures such as Stack,Queue can be easily implemeted using Linked list

- **DISADVANTAGES OF LINKED LIST:**

   1. Reverse Traversing is difficult if we are using singly linked list then it is very difficult to traverse linked list from end.
   2. Time Complexity Array can be randomly accessed , while the Linked list cannot be accessed Randomly
   3. No Random Access In Linked list no random access is given to user, we have to access each node sequentially.
   4. Wastage of Memory Pointer Requires extra memory for storage.
     
- **DIFFERENCES BETWEEN ARRAY AND LINKED LIST:**

1. An array is the data structure that contains a collection of similar type data elements whereas the Linked list is considered as non-primitive data structure contains a collection of unordered linked elements known as nodes.
2. In the array the elements belong to indexes, i.e., if you want to get into the fourth element you have to write the variable name with its index or location within the square bracket.
3. In a linked list though, you have to start from the head and work your way through until you get to the fourth element.
4. Accessing an element in an array is fast, while Linked list takes linear time, so it is quite a bit slower.
5. Operations like insertion and deletion in arrays consume a lot of time. On the other hand, the performance of these operations in Linked lists is fast.
6. Arrays are of fixed size. In contrast, Linked lists are dynamic and flexible and can expand and contract its size.
7. In an array, memory is assigned during compile time while in a Linked list it is allocated during execution or runtime.
9. Elements are stored consecutively in arrays whereas it is stored randomly in Linked lists.
10. The requirement of memory is less due to actual data being stored within the index in the array. As against, there is a need for more memory in Linked Lists due to storage of additional next and previous referencing elements.
11. In addition memory utilization is inefficient in the array. Conversely, memory utilization is efficient in the linked list.
