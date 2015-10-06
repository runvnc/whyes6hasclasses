# whyes6hasclasses

After seeing so much hate for classes in the Node community, I started re-thinking my enthusiasm.

## Returning an object from a factor function

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

But I am wondering then, what is the standarad way to inherit from a _something_ in ES6?  Is it `util.inherits`?  Is that in the spec?   Maybe I am just confused by that example.

So then I wondered if there was another better example that would explain the correct way to do this stuff in ES6.  So I googled 'React ES6' and found this blog entry at the top:



The answer is no, there is only one standard way to inherit from a _something_ in ES6.  That is using `class` and `extends` keywords.


