---  
layout: article  
title: "ArrayList indexOf() method"  
author: coderolls  
tags: 
- Collections
- ArrayList
toc: true  
description: "In this tutorial, we will see the  indexOf() method of the ArrayList class in Java."  
---
In this tutorial, we will see the `indexOf()` method of the  [ArrayList class in Java](https://coderolls.com/arraylist-in-java/). This method returns the index of the first occurrence of the specified element in this list.

## Introduction  
ArrayList is a widely used class to store and retrieve data in a collection framework.

Also, we have seen a few methods of the ArrayList class before like [`add()`](https://coderolls.com/add-element-in-arraylist/), [`addAll()`](http://https://coderolls.com/arraylist-addall-method-in-java/), [`remove()`](https://coderolls.com/remove-element-from-arraylist/), [`set()`](https://coderolls.com/change-element-in-arraylist/), [`iterate()`](https://coderolls.com/iterating-the-arraylist-in-java/), [`clear()`](https://coderolls.com/arraylist-clear-method-in-java/),  [`contains()`](https://coderolls.com/arraylist-contains-method), [`get()`](https://coderolls.com/arraylist-get-method), [`removeRange()`](https://coderolls.com/arraylist-removerange-method), [`retainAll()`](https://coderolls.com/arraylist-retainall-method) and [`trimToSize()`](https://coderolls.com/arraylist-trimtosize-method) method. 

Today we will see the `indexOf(Object o)` method.  
  

## ArrayList `indexOf(Object o)` method  

We know the important feature of the list is that it maintains the insertion order of the elements. Also, it allows duplicate elements in the list.

So, when we try to find any elements, there are chances that the same elements may present in the list multiple times at multiple indexes.

The `indexOf(Object o)` method **returns the index of the first occurrences of the object specified**. It **returns -1 if the specified object `o` is not present** in the list.

The method signature is given below.

```java
public int indexOf(Object o)
```
The `indexOf()` method accepts only one parameter, the `Object o` whose index of the first occurrence will be returned.

The method has a return type as an `int`. It returns the index of the first occurrences of the object specified as an `int` . If the specified object `o` is not present in the list, it will return -1.

Let's see the Java program for a better understanding.

```java
/**
 * A java program to explain the indexOf() method
 * of the ArrayList class in Java.
 * 
 * @author coderolls.com
 */
public class ArrayListIndexOfExample {

  public static void main(String[] args) {
    // create an empty ArrayList object 'states'
    List<String> states = new ArrayList<String>();
    
    // add state in the ArrayList, Florida multiple times
    states.add("California");
    states.add("Texas");
    states.add("Florida");
    states.add("Florida");
    states.add("New Jersey");
    states.add("Washington");
    states.add("Florida");
    
    int index = states.indexOf("Florida");
    
    //prints index of the first occurrences of Florida i.e. 2
    System.out.println("The index of Florida: "+ index);
    
    //trying to get the index of the element, which is not present
    int index2 = states.indexOf("Alaska");
    
    System.out.println("The index of Alaska: " + index2);
  }
}
```  

Output:  
```
The index of Florida: 2
The index of Alaska: -1
```

## Conclusion  

```java
public int indexOf(Object o)
```
The `indexOf(Object o)` method **returns the index of the first occurrences of the object specified**. If the specified object `o` is not present in the list, it returns the -1.

---

The example Java program used in the above article can be found at [this GitHub repository](https://github.com/coderolls/blogpost-coding-examples/tree/main/collections/arraylist/arraylist-indexof-method).  

Please write your thoughts in the comment section below.
