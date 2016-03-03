# this vs _this

When using fat arrows in Typescript, the compiler will create a hidden `_this` variable with lexical scope and replace calls to `this` with `_this`. If you want access to the global scope or give control to a library like d3, use normal javascript function syntax.

[Source](http://blog.simontimms.com/2013/01/28/this-vs-_this-in-typescript/)
