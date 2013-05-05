---
layout: post
title: "quick way to center an absolutely positioned element"
date: 2013-05-04 23:39
comments: true
categories: [css, code]
---

I find it hard to blog about technical related issues. I feel most of the time everything I have to say has already been said but this is something i've found a lot of my peers especially at the current company I work at weren't aware of... its a quick way to center an absolutely positioned element.<!-- more -->

The only real requirement for this is you need to know the width of the element. Here is an example:

{% codeblock %}
#sampleDiv {
	position: absolute;
	top: 30%;
	left: 50%;
	margin-left: 225px;
	width: 450px;
}
{% endcodeblock %}


That's it... you position the element left 50 percent and then create a negative margin of 1/2 the width of the element, and it works.

I was surprised to know that this was something a few people I work with weren't aware of so I thought I would share just in case anyone out there isn't aware of this technique.

- Be Awesome :)