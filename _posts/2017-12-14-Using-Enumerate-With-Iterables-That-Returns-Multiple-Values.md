---
layout: post
title: Using Python's Enumerate With Iterators That Returns Multiple Values
---
Lets say you are using an iterator that returns multiple values which you pass to function, like this,

    results = [myFun(val1,val2,...) for val1,val2,... in myIterable]

Now, the function value you return might depend on where you are in the iteration so we would like to pass an index value to the function. In Python we can do this with *enumerate*, for example, if we are creating a new array by multiplying each value in an array with its position in the array,

    result = [val*idx for idx,val in enumerate(myArray)]

To incorporate this into the iterable that returns multiple values we have to create a tuple,

    results = [myFun(val1,val2,...,idx) for idx,(val1,val2,...) in enuemrate(myIterable)]

Notice that even though the val1, val2... is inside the tuple we can still refer to them as arguments for the function. 
