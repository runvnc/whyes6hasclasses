# Why ES6 has Classes

After seeing so much hate for classes in the Node community, I started re-thinking my enthusiasm.

## Returning an object from a factory function

```javascript
function createPerson(firstName) {                                                                            
  return {                                                                                    
    sayHello: function() {                                                                                        
      setTimeout(() => {                                                                                          
        console.log("Hello, I'm " + firstName);                                                                       
      }, 50);                                                                                                         
    },                                                            
    test: 10                                                                                                          
  };                                                                                                                  
}                                                                                                                                                                       
var t = createPerson('ted');                                                                                            
t.sayHello();                
```

Works great.

## Who needs classes anyway?

So I started thinking, classes are a legacy concept. Returning an object from a function is how real JavaScript programmers do it. Then I looked on the Node.js page for Events: https://nodejs.org/api/events.html

Darn.  It says the word 'class' all over that page.  And the example uses `util.inherits`.  Maybe the use of the word 'class' was just a fluke, and they meant something else.  But I definitely have to inherit from a _something_ for events.  Whatever that is, its not a class, I am sure!  

## Node.js 'classes'?

But I am wondering then, what is the standard way to inherit from a _something_ in ES6?  Is it `util.inherits`?  Is that in the spec?   Maybe I am just confused by that example.

So then I wondered if there was another better example that would explain the correct way to do this stuff in ES6.  So I what's the second most popular system using JavaScript these days?

## React.js 'classes'??

So I googled 'React ES6' and this blog entry came up: https://facebook.github.io/react/blog/2015/01/27/react-v0.13.0-beta-1.html

> So what is that one feature I'm so excited about that I just couldn't wait to share?

> Plain JavaScript Classes!!

> JavaScript originally didn't have a built-in class system. Every popular framework built their own, and so did we. This means that you have a learn slightly different semantics for each framework.

> We figured that we're not in the business of designing a class system. We just want to use whatever is the idiomatic JavaScript way of creating classes.

Wait a minute.. this guy has no idea what he is talking about.  Who is this guy?  Hmm.. weird.  It says he is an engineer at Facebook.  I thought they had better screening than that??  I mean, he doesn't even know JavaScript!  He thinks JavaScript should have classes!  They should fire him!

## What the heck is going on?

So here we have probably the two most popular JavaScript systems in the world in Node.js and React and one has documentation full of the word 'class' and on the other a developer _openly admits to being excited about classes and even uses 'class' and 'extend' in a code example_!??

How can this be?? Do all of these Node and React guys just not know how real JavaScript programmers code??  Surely someone would have clued them in by now that you aren't inheriting from 'classes', you are using prototypes (or something).

## The answer

The answer is that _classes and inheritance are core aspects of JavaScript development and there is a standard way to do them in ES6 using the `class` and `extends` keywords_.

