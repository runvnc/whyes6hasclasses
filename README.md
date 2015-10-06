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

So I started thinking, classes are a legacy concept.  Then I looked on the Node.js page for Events: https://nodejs.org/api/events.html

