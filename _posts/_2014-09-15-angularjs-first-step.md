---
layout: post
title: Angular.js overview
categories: javascript angular 
tags : javascript, angular
excerpt: An overview of angular.js from starting to building, throught testing and architecture
---


# Purpose
Angular.js is a Javascript Framework that you have certainly heard about.

We've using it for a year @Youboox and we manage a big web app, with a lot of screen, external library, security issues and other cool stuff.

So I tought it would be cool to share some experience.

You can contact me at boris@youboox.fr.

# Why it's fun

You can find a lot of website explaining binding and top 10 of why angular is great.

That's not our main purpose here, so let's be quick, shall we.

## Binding
Yes with angular you can actually bind a variable in javascript and exploit it in your html.
What does that mean : 

In a javascript file (more on the $scope later) : 

{% highlight javascript %}

$scope.welcome_message = "Hello world";

{% endhighlight %}

In the html counterpart : 

<pre>

&lt;div&gt;
&lt;p&gt; &#123;&#123; welcome_message &#125;&#125; &lt;/p&gt;
&lt;/div&gt;

</pre>

And your html will actually show "Hello World"

In angular you're not going to manipulate DOM to show a text or display something, and it's a HUGE advantage because it eliminate a lot of glue code where you would have to access an element to manipulate it's content.

It untie in your code the HTML and the Javascript, you html can change, you just have to replace the variable.

In fact, it's often our DA that write the HTML and we just have to pass througt the content to put some variable and action, and the work is done.

## Injection

We will talk about it later, but to be short, when you name something, just pass that name around, and it will magically be loaded.

Imagine an Angular Constant (more on it later)

{% highlight javascript %}

module.constant('MySuperConstant', function(){ return "YEAH";});

{% endhighlight %}

In a Controller : 

{% highlight javascript %}

module.controller(function($scope, $q, $MySuperConstant){
    
    console.log($MySuperConstant); // will show YEAH
});

{% endhighlight %}






## Testing
Simple to test !

## Organizing
There is an architecture.

# Why it's less cool

## Performances
Try big list.

## Directives are complicated
scope madness, not really angular.

## It doesn't like stranger
Try integrating with something else

# Starting with Yeoman

Create all your project with a simple command line.
Scaffold what you need, force you to do good practice to start with.
You can use require js.

# Architecture

No model, controllers, clear separation of responsability, reusable component with directives.

## Controllers

### Scope

{% highlight javascript %}

    $scope.welcome_message = "Hell world";

{% endhighlight %}

## Services
Communicate beetween controllers.
Reuse code.
Separation of responsability.

## Directives
Put the DOM there.

## Puting it all together

Service who fetch json, add it to array, show it with ng-repeat.

# Quick talk about Promise

Remade the service with promise syntax.

# Test & Continuous integration

## Karma

## Testing Service

## Testing Controller

# Building



