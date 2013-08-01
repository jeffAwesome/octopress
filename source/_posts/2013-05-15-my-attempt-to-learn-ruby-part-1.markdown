---
layout: post
title: "My attempt to learn Ruby Part 1"
date: 2013-05-15 22:20
comments: true
categories: [rails, 'rails and Javascript']
---


In the constantly changing area of front end web development there may be a time when you have to at the very least understand the basics of a backend language such as ruby. I am going to use a language all front end developers should know... Javascript to help me and hopefully you understand the funadmentals of ruby... lets dig in.<!--more-->

##Understanding Ruby through Javascript
When you aren't a 'true' programmer by nature learning a new language can be intimidating, especially when its a backend language... but after several hours of blindly reading I started taking notes and comparing it to a language I already know very well... Javascript. A lot of what I have below is mainly just rough notes I made from reading through the book I previously mentioned. It may not help you at all but it seems to be the trick I needed to grasp the new language.

##Lets start with null and nil
In javascript we have null in Ruby we have nil... for the most part they are the same. And the interesting thing about it is they are both objects. Everything in ruby is an object but to test in Javascript.. simply try this in the console.


	typeof null;
	/* It will return object. */

## Methods
So far from my understanding a method in ruby is a lot like a function in javascript. Consider the following example in javascript:

	function say_goodnight(name) {
		var result = 'Good Night' + name;
		return result;
	}

	/* Then you could call that function like so: */

	say_goodnight('John-Boy');
	say_goodnight('Mary-Ellen');

In ruby it looks like this:

	def say_goodnight(name)
   		result = 'Good night, ' + name
   		return result
	end

	/* and you'd call it like so */

	puts say_goodnight('May-Ellen')
	puts say_goodnight('John-Boy')

In ruby the semi colons are optional as long as each statement is in a new line.


##Arrays and Hash
Arrays in ruby and javascript are very similar

in javascript its

	a = [1, 'cat', 3.14];

	/* You can access them in javascript with */

	a[0];

	/* and can assign a value like so */

	a[2] = null;

in ruby its 

	a = [1, 'cat', 3.14]
	a[0]  
	a[2] = nil

###What the heck is a hash?
This was the exact thing I thought when it was first mentioned but in ruby it is very similar to an array. It looks almost identical to a Javascript object on first look. In Javascript you can define Objects, which are the closest things to an associative array for the language.

A javascript object

	theJsObject = {
		shoppingCart: 'shopping cart value',
		anotherSymbol: 'another value'
	}

	/* To Access a value with Javascript  */

	theJsObject.shoppingCart
	/* or */
	theJsObject['shoppingCart']
	/* Returns shopping cart value */

In Ruby a Hash looks like this:

	the_hash_example = {
		:shopping_cart => 'shopping cart value',
		:another_symbol => 'another value'
	}

	/* To grab a value from the hash you would simply do the following */

	the_hash_example[:shopping_cart] 
 	/* Returns shopping cart value */

See how similar to a Javascript object it is? You can even grab a value in javascript an almost identical way.
I know that they aren't the same thing but it helps me start to wrap my mind around what's going on with ruby and some of its language fundamentals.



##Comparing Helps me maybe it helps you.
When first reading through the code I was simply seeing the code but when I think about it and compare it to something I alredy know it does wonders... the ruby code makes so much more sense... now I understand that I am probably over simplifying what's happening and I may even be mis-stating something and if so **please let me know**, but overall this is helping me grok the fundamentals of the language.

##Whats next?
In the next post I will be going over differences and similarities with control statements between the two languages.


Be Awesome.

