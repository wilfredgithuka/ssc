---
title: "Mapping Tools & Skills in Python"
date: 2019-04-26T06:07:55Z
draft: false
---

After spending a good easter weekend becoming familiar with shapefiles in
python basemap, it is clear that there was alot that I have to learn
in order to map the schools well.

This is a part of a series of posts of my project to map technical training schools according to the equipments that they have. I suggest you look at these posts then follow on to know what am talking about:

* [Mapping Welding Training Schools in Kenya With Python Basemap](https://chinese.githuka.com/blog/ditu/)
* [Working With Kenya County Shapefiles](https://chinese.githuka.com/blog/ditu_county_shapefiles/)
## Data Structures

In CS data structures are ways to organaize data in a computer that makes t computationaly efficient. Data structures are very important and really shows the think pattern that the programmer used to arrive at the solution. In maping I will talk about 3 parts:

* Python Lists
* Python Tuples
* Python Dictionaries

### Python Lists

Python list is a most versatile datatype available in Python which can be written as a list of comma-separated values (items) between square brackets. Important thing about a list is that items in a list need not be of the same type. Python lists are designated with square brackets.

```
a = []
b = ['me', 'you','wo'i]
```

In lists, the value of the first item is a 0. So to check the contents of a list, you can pass this statement.

```
b[1]
```
Which will give: you

### Python Tuples

A tuple is like a list but its immutable. Not changeable. A tuple is represented by brackets as opposed to lists which have square brackets. Tuples are therefore good for storing immutable values like the GPS co-ordinates for the various schools that I need to map. :-). Working with tuples is preety easy:

```
a = ()
b = (32, 41)
c = ('x', 'y')
```
To access an element in a tuple, simply issue the following command:

```
b[1]
```
Which will result: 41

### Python Dictionaries
Also known as associative arrays, maps, symbols tables or hash tables. Dictionaries are computationaly fast but on the other hand use alot of memory. They contain key:value pairs. Here is an example on working with dictionaries.

```
dict_a = {}
dict_b = {'Hey Wilfred':'How are you?'}
```
In the above example, the key is: Hey Wilfred and the value is: How are you. Once you understand this, then you can call the key like this:

```
dict_b['Hey Wilfred']
```
This will result: 'How are you?'

After understanding this concepts, we can now go to preparing the data.

Remember, if you have any issues on Python, always go to the python documentation page which has tonnes of info which I think will be of great help before stack-overflow.

Back to code :-)
