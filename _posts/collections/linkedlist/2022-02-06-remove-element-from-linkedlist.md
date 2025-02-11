---
layout: article
title: "How To Remove Element From LinkedList?"
author: gaurav
tags: 
- Collections
- LinkedList
toc: true
description: "In this article, we will see, how to remove an element from the LinkedList. The LinkedList class provide various methods to remove an element from the LinkedList. We will cover these methods with examples."
---

In this article, we will see, how to remove an element from the LinkedList. The LinkedList class provide various methods to remove an element from the LnikedList. We will cover these methods with examples.

## Introduction

The LinkedList class is present in the `java.util` package.

[LinkedList](https:/coderolls.com/linkedlist-in-java/) internally uses doubly LinkedList for storing the variables. That's why LinkedList is preferred when our frequent operation is insertion and deletion.

The LinkedList class has the following methods to remove the object from the LinkedList.

1. `remove()`
2. `remove(Object o)`  
3. `remove(int index)` 
4. `removeFirst()`  
5. `removeLast()`

Let's see all these methods one by one.  

## 1. `remove()`

The `remove()` method **retrieves and removes the head (first element) of this list**.

The method signature for the `remove()` method is given below.

```java
public E remove()
```

This method **returns the head(first element) of this list**. And it does not accept any parameter.

I have given a sample Java program to remove an element from the list using the `remove()` method.

```java
import java.util.LinkedList;

/**
 * A Java program to remove a head element from 
 * the linkedList using the remove() method.
 * 
 * @author coderolls.com
 *
 */
public class LinkedListRemove {

  public static void main(String[] args) {
    LinkedList<String> linkedList = new LinkedList<String>();
    
    linkedList.add("BHIM");
    linkedList.add("PayTM");
    linkedList.add("Freecharge");
    linkedList.add("PhonePe");
    linkedList.add("JioPay");
    
    System.out.println("LinkedList before removing an element:");
    System.out.println(linkedList);
    
    // removes head(first element) i.e. removes BHIM
    linkedList.remove();
    
    System.out.println("\nLinkedList after removing an element using remove() method:");
    System.out.println(linkedList);
  }
}
```

Output:

```
LinkedList before removing an element:
[BHIM, PayTM, Freecharge, PhonePe, JioPay]

LinkedList after removing an element using remove():
[PayTM, Freecharge, PhonePe, JioPay]
```

### Exceptions

The `remove()` method throws [`NoSuchElementException`](https://docs.oracle.com/javase/7/docs/api/java/util/NoSuchElementException.html) if this list is empty.

## 2. `remove(Object o)`  

The `remove(Object o)` method **removes the first occurrence of the specified element in a list, if it is present**.

If the list does not contain the specified element, there will be no change in the list.

The method signature for the `remove(Object o)` method is given below.

```java
public boolean remove(Object o)
```

This method accepts a parameter Object `o`, which needs to be removed from the list.

This method **returns a boolean value**. It will return **`true`** if the list got changed as a result of this method call, otherwise **`false`**.

I have given a sample Java program to remove an element from the list using the `remove(int index)` method.

```java
import java.util.LinkedList;

/**
 * A Java program to remove the specified element from 
 * the linkedList using the remove(Object o) method.
 * 
 * @author coderolls.com
 *
 */
public class LinkedListRemoveObject {

  public static void main(String[] args) {
    LinkedList<String> linkedList = new LinkedList<String>();
    
    linkedList.add("BHIM");
    linkedList.add("PayTM");
    linkedList.add("Freecharge");
    linkedList.add("PhonePe");
    linkedList.add("JioPay");
    
    System.out.println("LinkedList before removing an element:");
    System.out.println(linkedList);
    
    // removes the specified element i.e. removes Freecharge
    linkedList.remove("Freecharge");
    
    System.out.println("\nLinkedList after removing an element using the remove(Object o) method:");
    System.out.println(linkedList);
  }
}
```

Output:

```
LinkedList before removing an element:
[BHIM, PayTM, Freecharge, PhonePe, JioPay]

LinkedList after removing an element using the remove(Object o) method:
[BHIM, PayTM, PhonePe, JioPay]
```

### Exceptions

The `remove()` method throws [`NoSuchElementException`](https://docs.oracle.com/javase/7/docs/api/java/util/NoSuchElementException.html) if this list is empty.

##  3. `remove(int index)` 

The `remove(int index)` method **removes the element at the specified position (`index`) in this list.**

Once, this method removes the element, it shifts any subsequent elements to the left (subtracts one from their indices).

The  method signature for the `remove(Object o)` method is given below.

```java
public E remove(int index)
```

This method **returns the element that was removed from the list**.

I have given a sample Java program to remove an element from the list using the `remove(int index)` method.

```java
import java.util.LinkedList;

/**
 * A Java program to remove elements at the specified position i.e. index
 * from the linkedList using the remove(int index) method.
 * 
 * @author coderolls.com
 */
public class LinkedListRemoveObjectByIndex {

  public static void main(String[] args) {
    LinkedList<String> linkedList = new LinkedList<String>();
    linkedList.add("BHIM");
    linkedList.add("PayTM");
    linkedList.add("Freecharge");
    linkedList.add("PhonePe");
    linkedList.add("JioPay");
    
    System.out.println("LinkedList before removing an element:");
    System.out.println(linkedList);
    
    // removes the element at index 3 i.e. removes PhonePe
    linkedList.remove(3);
    
    System.out.println("\nLinkedList after removing an element using the remove(int index) method:");
    System.out.println(linkedList);
  }
}
```

Output:

```
LinkedList before removing an element:
[BHIM, PayTM, Freecharge, PhonePe, JioPay]

LinkedList after removing an element using the remove(int index) method:
[BHIM, PayTM, Freecharge, JioPay]
```

### Exceptions

The `remove(int index)` method throws [`IndexOutOfBoundsException`](https://docs.oracle.com/javase/7/docs/api/java/lang/IndexOutOfBoundsException.html) - if the index is out of range (`index < 0 || index >= size()`)

## 4. `removeFirst()` 

The `removeFirst()` method **removes and returns the first element from this list**.

The  method signature for the `remove(Object o)` method is given below.

```java
public E removeFirst()
```

This method does not accept any parameter and it will **return the first element from this list**.

I have given a sample Java program to remove the first element from the list using the `removeFirst()` method.

```java
import java.util.LinkedList;

/**
 * A Java program to remove the first element from 
 * the linkedList using the removeFirst() method.
 * 
 * @author coderolls.com
 *
 */
public class LinkedListRemoveFirst {

  public static void main(String[] args) {
    LinkedList<String> linkedList = new LinkedList<String>();
    linkedList.add("BHIM");
    linkedList.add("PayTM");
    linkedList.add("Freecharge");
    linkedList.add("PhonePe");
    linkedList.add("JioPay");
    
    System.out.println("LinkedList before removing an element:");
    System.out.println(linkedList);
    
    // removes first element i.e. removes BHIM
    linkedList.removeFirst();
    
    System.out.println("\nLinkedList after removing an element using the removeFirst() method:");
    System.out.println(linkedList);
  }
}
```

Output:

```
LinkedList before removing an element:
[BHIM, PayTM, Freecharge, PhonePe, JioPay]

LinkedList after removing an element using the removeFirst() method:
[PayTM, Freecharge, PhonePe, JioPay]
```

### Exceptions

The `remove()` method throws [`NoSuchElementException`](https://docs.oracle.com/javase/7/docs/api/java/util/NoSuchElementException.html) if this list is empty.

## 5. `removeLast()`

The `removeLast()` method **removes and returns the last element from this list.**

The  method signature for the `removeLast()` method is given below.

```java
public E removeLast()
```

This method does not accept any parameter and it will **return the last element from this list**.

I have given a sample Java program to remove the last element from the list using the `removeLast()` method.

```java
import java.util.LinkedList;

/**
 * A Java program to remove the last element from 
 * the linkedList using the removeLast() method.
 * 
 * @author coderolls.com
 *
 */
public class LinkedListRemoveLast {

  public static void main(String[] args) {
    LinkedList<String> linkedList = new LinkedList<String>();
    linkedList.add("BHIM");
    linkedList.add("PayTM");
    linkedList.add("Freecharge");
    linkedList.add("PhonePe");
    linkedList.add("JioPay");
    
    System.out.println("LinkedList before removing an element:");
    System.out.println(linkedList);
    
    // removes first element i.e. removes BHIM
    linkedList.removeLast();
    
    System.out.println("\nLinkedList after removing an element using the removeLast() method:");
    System.out.println(linkedList);
  }
}
```

Output:

```
LinkedList before removing an element:
[BHIM, PayTM, Freecharge, PhonePe, JioPay]

LinkedList after removing an element using the removeLast() method:
[BHIM, PayTM, Freecharge, PhonePe]
```

### Exceptions

The `remove()` method throws [`NoSuchElementException`](https://docs.oracle.com/javase/7/docs/api/java/util/NoSuchElementException.html) if this list is empty.

## Conclusion

In the above tutorial, I have shared 5 methods to remove an element from the LinkedList. These 5 methods are as given below.

1. `remove()` - Retrieves and removes the head (first element) of this list. 

   ```java
   //head (First element) will be removed from the LinkedList 
   linkedList.remove();
   ```

2. `remove(Object o)`  - Removes the first occurrence of the specified element in a list.

   ```java
   //'obj' will be removed form the linkedList
   linkedList.remove(obj);
   ```

3. `remove(int index)` - Removes the element at the specified position in this list.

   ```java
   //The element at index 3 will be removed from the LinkedList 
   linkedList.remove(3);
   ```

4. `removeFirst()`  - Removes and returns the first element from this list.

   ```java
   // first element will be removed from the LinkedList 
   linkedList.removeFirst();
   ```

5. `removeLast()` - Removes and returns the last element from this list.

   ```java
   // last element will be removed from the LinkedList 
   linkedList.removeLast();
   ```

---

The example java programs given in the above tutorial can be found at [this GitHub Repository](https://github.com/coderolls/blogpost-coding-examples/tree/main/collections/LinkedList/remove-element-from-linkedlist).

Let me know you thoughts or suggestions on the topic discussed above in comment section below.
