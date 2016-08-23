---
layout: post
title:  "I'm Learning basics of Object Oriented Programming"
date:   2016-08-23 19:30:12 +0000
---

I will begin by stating that I felt like I was in Inception when I began object orient programming.  There were many instances, variables and methods to the point where differentiating gave me minor headaches.

Often referred to as OOP, object oriented programming is a paradigm created to handle the growing complexity of software systems at large.  Early on programmers found that as applications grew with size and complexity, it became very difficult to maintain.  A simple, small change any point in a program would trigger a ripple effect of errors due to the entire program's dependencies.

Because of this, programmers needed to section off parts of code that would perform specific procedures so the program would become the interaction of many parts, instead of one, giant program of dependency.  Programmers needed to create containers for data that could be modifed without affecting the entire program.

I present to you Object Oriented Programming.

### Ruby's Objects
Often you'll hear in the Ruby community "Everything is an object in Ruby!" Right now it's neccessary to get a handle of the basic Ruby syntax before thinking of objects.

Overall it is true, everything in Ruby is an object.  These objects are created from classes.  You can think of classes as a cookie cutter and the objects are the thngs created from the cookie cutter.  Each individual object contains different information yet they are intances of the same class.  Below is an example of the String class.  This example shows us using the class method to determine what class is for each object.  As you can see, what we've been using, from strings to integers, are objects that are instantiated from a class. I'll touch on instantiation soon.

![](https://s20.postimg.org/srk1y4y8t/oo_blog.jpg)

### Objects Defined by Class
Attributes and behaviors are defined in Ruby by classes.  It's simply a basic outline of what the object should be made of and what it's capable of doing.  When defining a class we use the syntax similar to defining a method.  We replace *def* with *class* and use the CamelCase naming format to create the name.  We finish the definition with *end*.  File names in Ruby should be *snake_case* and reflect the class name.  In my example below, I'm not using the *snake_case* format but the filename matches the class name.

![](https://s20.postimg.org/he240od3x/oo_blog_filename.jpg)

In your Class you can began building your objects with methods and instances.  Here I'm going to show you step by step how an object is born.

![](https://s20.postimg.org/4jzgtlaal/oo-blog-instantiating.jpg)

In the example above, I am creating many new instances of the Fashionistas class with each object being stored in the variable of the blogger's name.  The workflow of creating a new object or instance from a class is called instantiation.  The important fact here is the object is returned by calling the class method *.new*.  Here each blogger is instantiated with four arguments, or attributes.  You can see that defining and creating a new instance of a basic class is simple.

![](https://s20.postimg.org/kfoaww0v1/oo_blog_initialize.jpg)

Above I have built an initialize method.  For every new object I want to create, I want it to have these four traits that essential to the new object.  You can also see that I have built a variable that will continue to collect every new object created.  For my Fashionistas class it is important that each "blogger" object have a name, the name of their blog, their origin of country and their age.

![](https://s20.postimg.org/dle07787x/oo-blog-attr-accessor.jpg)

At the beginning of my class, in the example above, you can see that I have built simple code using *attribute_accessors* simply formatted at *attr_accesor*.  This is Ruby magic.  Accessor has a built-in pair of *setter* and *getter* methods.  Without the use of accessor I would have very long, redundant code for each attributes of the bloggers.  Below is a short example of building a setter method and a getter method.  Imagine how long my Class would be if I also wrote setter/getter methods for blog_name, origin and age, it's long, trust me.

![](https://s20.postimg.org/7n06wyp99/oo_blog_getter.jpg)

If everytime I wanted each blogger to express their love of fashion, I could build an instance method to have the bloggers do just that.  They are able to express any behavior in the Fashionistas class.  Here I have them simply quote "I love fashion!" when called upon.

![](https://s20.postimg.org/qhvxndpb1/oo-blog-instance.jpg)

These are the few, simple steps when creating a Class.  A class can be a simple or complex as you would like it.  I'm learning still on how to build classes and how to collaborate with other objects.  For now I'll leave at this.

Happy Coding!




