---
layout: post
title:  "The art of writing quality CSS"
description:  "The steps I am trying to follow while I am working one of my first big front-end projects."
date:   2015-02-13 10:00:00
categories: blog
---

CSS is one of the most under-looked phenomenon in while we as developers start building something new. The idea is simple, we have to ship and in order to do that we make something which is *just* about working.

I have been building for the internet from a couple of years now. Honestly, I have written some really ugly CSS in the past and cursed myself everytime as the codebase increased. Most of the time, I was working on the same issues again and again so I decided to create my personal CSS styleguide which helps each time I start building anything new. Here are a couple of fun facts from my CSS styleguide:

1. ### Fluid(%) Vs. Not Fluid(px)

	Take a call *before* you write your first line of CSS. Whenever we go full fluid, the physical dimensions, (*mainly widths*) are written in percentages, otherwise hard values ( *such as px, em, etc.* ) are used. Mixing up between the two would eventually result in overlapping between different grids for obvious reasons. The only hard values to be used in fluid layouts are the maximum or the minimum widths at break points, you don't need them, practically anywhere.

	Let me give you two examples:-

	- **[Zomato](http://www.zomato.com)** is one popular startup which *definitely* has made my life simple with its amazing restaurant listings. The concept, the UI is brilliant on my Mac, but one fine day while I was working, I had my screen resized to 992px (*it's not too small*) the navigation jumped down whereas the remaining elements of the entire web page seemed intact. A very small issue, which breaks the entire home page, atleast.

	{% include images.html url="../../../../../images/zomatoscreenshot.png" description="Breaking Dawn for Zomato" %}

	- **[Practo](https://www.practo.com/)** is another startup which is on a rise with the medical industry. I have not used the application dedicatedly but their website seemed to extremely impressive. It's responsive, not fluid, and handles it brilliantly at smaller widths. Even going from its stylesheets, it seemed *really* impressive.

	{% include images.html url="../../../../../images/practoscreenshot.png" description="Practo steals the show" %}

2. ### Don't use a UI toolkits you don't intend to use them in future

	There are moments when I have to prototype, those times I love uisng Twitter Bootstrap, the remaining times I simply hate it **to the core**. Initially, when I was dependant on twitter bootstrap and used it extensively, I spent **much** more time overridding the simple changes it comes along with than writing my own CSS. It's definitely an overkill, if you have plans of writing your own styles.

3. ### The lesser, the better

	Unlike programming languages, say JavaScript, when you are writting CSS, you can take my word that

	> **Lesser CSS = Better CSS**

	The easiest way to write better *or lesser* CSS is to keep your *global classes* ready.
	As an extremely simple example:

		.logo {
		  float: left;
		  margin-left: 10px;
		  padding: 10px 20px;
		}
		.widget {
		  float: left;
		  margin-left: 0;
		  width: 30%;
		}

	**This sucks.**

		.logo {
		  margin-left: 10px;
		  padding: 10px 20px;
		}
		.widget {
		  margin-left: 0;
		  width: 30%;
		}
		.pull-left {
		  float: left;
		}

	**This is *so* much better.**

	Now, this class is ready to be used anywhere, where the need of *pulling* content to left is need. I call such classes **global classes**. These classes will significantly reduce the number of lines of your CSS.

4. ### Use multiples of 5 (or something else, *may be 4*)

	I have quoted it in my previous blog posts too that everything can positioned pixel perfectly if written in *standard* multiples. There is no point of going 23px left or 32px right. If you are doing it, you are doing it wrong.

5. ### Maintain a standard class naming convention

	Don't name your classes haphazardly, follow a naming convention.


Notice that in my entire post, I didn't even try to use the term **id** or the *#hashtag*. There is a reason, they suck. If you are using an ID, you are probably not using your global classes effectively. Ids are extremely specific, so spare them for the JavaScript.

Talking about specifivity, [here](http://csswizardry.com/2014/10/the-specificity-graph/) is an awesome post by Harry Roberts. You should give it a read.

