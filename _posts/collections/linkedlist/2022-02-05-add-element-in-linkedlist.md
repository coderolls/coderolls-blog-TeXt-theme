---
layout: article
title: "How To Add Element To LinkedList?"
author: gaurav
tags: 
- Collections
- LinkedList
toc: true
description: "In this article, we will see, how to add an element to LinkedList. The LinkedList class provide various methods to add an element to the LnikedList. We will cover these methods with examples."
---

In this article, we will see, how to add an element to LinkedList. The LinkedList class provide various methods to add an element to the LnikedList. We will cover these methods with examples.

## Introduction

The LinkedList class is present in the `java.util` package.

[LinkedList](https:/coderolls.com/linkedlist-in-java/) internally uses doubly LinkedList for storing the variables. That's why LinkedList is preferred when our frequent operation is insertion and deletion.

We can add an element to the LinkedList using the `add()` method. There are two types of the `add()` method.

1. `add(E e)`
2. `add(int index,E element)`
2. addFirst(E e)
2. addLast(E e)

The `add()` method will append an element to the end of the list. The `add(int index, E element)`  method will add the element at the specified index `index`.

Since LinkedList internally use a doubly LinkedList structure to store data, it provides two additional methods to add the elements using `addFirst(E e)` and `addLast(E e)`

Let's see both the methods one by one.

## 1. `add(E e)`

The method signature for this is given below,

`public boolean add(E e)`.

This method appends the specified element `e` to the end of the list.

This method returns `true` if the element is added to the list otherwise, it returns `false`.

I have given a Java program to add an element to the end of the list using the `add(E e)` method.

```java
import java.util.LinkedList;

/**
 * A Java program to add an element to the LinkedList.
 * 
 * The add(E e) method will add an element to 
 * the end of the LinkedList.
 * 
 * @author coderolls.com
 *
 */
public class LinkedListAddExample {
  public static void main(String[] args) {
    LinkedList<String> linkedList = new LinkedList<String>();
    
    //Adding elements to the LinkedList
    linkedList.add("John");
    linkedList.add("Peter");
    
    System.out.println(linkedList);// [John, Peter]
    
    //Adding an element to the LinkedList
    //Element will be added to the end of the LinkedList
    linkedList.add("Noah");
    
    System.out.println(linkedList); // [John, Peter, Noah]
  }
}
```

Output:

```
[John, Peter]
[John, Peter, Noah]
```

## 2. `add(int index, E element)`

The method signature for this method is given below.

````java
public void add(int index, E element)
````

This method adds the specified element `element` at the specified index `index`.

This method has a return type as `void` so, it will not return anything.

Below, we will see a Java program to add an element at the specified index in LinkedList.

```java
import java.util.LinkedList;

/**
 * A Java program to add an element to the LinkedList
 * at the specific index.
 * 
 * The add(int index, E element) method will add 
 * an element at the specified index in LinkedList.
 * 
 * @author coderolls.com
 *
 */
public class LinkedListAddExample2 {

  public static void main(String[] args) {
    LinkedList<String> linkedList = new LinkedList<String>();
    
    //adding elements to the linkedList using the normal add method
    linkedList.add("John");
    linkedList.add("Peter");
    linkedList.add("Karan");
    
    System.out.println(linkedList);// [John, Peter, Karan]
    
    // adding an element to  the LinkedList at index 1
    linkedList.add(1, "Noah");
    
    System.out.println(linkedList); // [John, Noah, Peter, Karan]
  }
}
```

Output:

```
[John, Peter, Karan]
[John, Noah, Peter, Karan]
```



## 3. [`addFirst(E e)`](https://coderolls.com/linkedlist-addfirst-method/)

We know that LinkedList internally uses the doubly linkedlist structure to store the data. To provide features like a doubly LinkedList, the LinkedList class has a special [`addFirst(E e)`](https://coderolls.com/linkedlist-addfirst-method/) method to add the element at the beginning of the list.

I have written a separate detailed article about the [`addFirst(E e)`](https://coderolls.com/linkedlist-addfirst-method/) method. Read [How To Add Element At The Beginning Of LinkedList?](https://coderolls.com/linkedlist-addfirst-method/)

## 4. [`addLast(E e)`](https://coderolls.com/linkedlist-addlast-method/)

We know that LinkedList internally uses the doubly linkedlist structure to store the data. To provide features like a doubly linkedlist, the LinkedList class has a special [`addLast(E e)`](https://coderolls.com/linkedlist-addlast-method/) method to add the element to the end of the list.

This method is equivalent to the `add(E e)` method.

I have written a separate detailed article about the [`addLast(E e)`](https://coderolls.com/linkedlist-addlast-method/) method. Read [LinkedList addLast(E e) Method](https://coderolls.com/linkedlist-addlast-method/)

## Conclusion

We can add an element to the [LinkedList](https://coderolls.com/linkedlist-in-java/) using the `add()` method in two ways.

1. `add(E e)` - It will add an element to the end of the LinkedList
2. `add(int index, E element)`- This method will add an element to the specified index
2. [`addFirst(E e)`](https://coderolls.com/linkedlist-addfirst-method/) - This method will add an element at the beginning of the list
2. [`addLast(E e)`](https://coderolls.com/linkedlist-addlast-method/) - This method will add an element to the end of the list

---

The example Java programs given in the above tutorial can be found at [this GitHub Repository](https://github.com/coderolls/blogpost-coding-examples/tree/main/collections/LinkedList/add-element-in-linkedlist).

Let me know your thoughts or suggestions on the topic discussed above in the comment section below.
