---
layout: post
title: Learning Angularjs in the field
categories: Javascript Angularjs 
tags : Angularjs
excerpt: Angularjs is great at first sight, but come with his load of tradeoff and complexity that you should be aware of
---


# Purpose
Angular.js is a Javascript Framework that you have certainly heard about.

We've using it for a year and a half [@Youboox](http://lire.youboox.fr) and we manage a big web app, with a lot of screen, external library, security issues and other cool stuff.

So I tought it would be cool to share some experience.

This is the first article.

You can contact me at [boris@youboox.fr](mailto:boris@youboox.fr).

# Learning angular in the field

Angular have a strange learning curve where the start is magic : 

* Ho my god it feel so clean and architectured.
* No DOM manipulation ? what is this magic ?
* Promise ? Ho my, that's beautifull.
* Test, you said test in javascript ? I love you.
* Magically inject dependancies.

You wait for a while at a plateau where you : 

 * try to integrate other not angular script not understanding why on earth it's not showing on your html.
 * discover directives. And their scope.
 * finally understand what the hell means [prototype-based language](http://en.wikipedia.org/wiki/Prototype-based_programming)
 
After that you have a better view of the all thing : 

* The magic behind No Dom manipulation is great but come at the cost of performances and there is actually really few thing you can do to overcome that.
* The injection mecanism is great untill you try to minify your code or have two services with the same name.
* Testing an angular app is actually quite simple. After you successfully configure it. If you don't come from the javscript world sit tight.
* Promise are still cool
* Make someone enter the code base and gaining new skill is strange : it will be eficient from week one but will need a month to understand all the subtlety that make him fully autonomous.
* The gain of no glue code for DOM manipulation, network call with promise, the add of architecture, directive to reuse html, and easy way to animate all this with ng-animate is a huge advantage.  


To further experience how other understand angular I made the experience to answer question on stackoverflow for a week on the angular subject. What I saw there is that there is : 

* A lot of question with misusage of directives
* A lot of question with misusage of promise
* A lot of question about testing (configuration, asynchronous etc..)
* A big lot of question about scope (inheritence, dom actualisation etc..)

And when people I know try angular for the first time THE first problem they tell me is : 
* I'm using the library X and I think I'm doing all good but my HTML is not changing.

So I guess the less obvious part of angular are : 

* How angular internaly work to render the dom.
* Prototypical inheritence.
* Directives.
* Promise.
* Karma configuration and jasmine test.

If you'r starting angular I recommand you read on the first and second point : 

* [https://docs.angularjs.org/guide/scope]()
* [http://javascript.info/tutorial/inheritance]() notably the little note that says that reading looks up, writing doesn't.

For Directives and promise you can read the doc, but I think it's experience that will help most...

* [https://docs.angularjs.org/guide/directive]()
* [https://docs.angularjs.org/api/ng/service/$q]()

So to synthetize my experience I would say that : 

* Angular actually have a moderate entry cost with a deferred payment. Don't think it's all simple and easy.
* You will have a hard time manipulate directives the first time.
* If the core of your product is to be amazingly fast maybe there is a better tool for you.
* I will still use Angular in the future and I'm really happy with our technological choice.

