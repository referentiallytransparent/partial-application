# What is this?
Partial Application is the technique of translating the evaluation of a function that takes multiple arguments (or a tuple of arguments) into evaluating a sequence of functions.

# Requirements
strict mode and support for the let keyword. The function can be changed to use var instead of let to preserve backwards compatibility. Probably another TODO for me

### Sample usage (TODO: improve)
```
'use strict';
let partiallyApply = require('./partiallyApply');

//normal function whose arguments we will partially apply
function add(a, b, c) {
    return a + b + c;
}

//supply all arguments
console.log((partiallyApply(add, 3, 4, 5)));

//supply 2 arguments for now
let partially2ArgAppliedAdd = partiallyApply(add, 3, 4);

//supply the 3rd argument later
console.log(partially2ArgAppliedAdd(5));
```

