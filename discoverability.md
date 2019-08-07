The more discoverable your code is, the less another developer needs to read through documentation or sift through legacy code to find what they are looking for. In worst case, if your code isn't discoverable enough, other developers may end up reimplementing existing functionality to acheve their goals.

## Enums instead of literals
If you have a set of options represented by literals, for example ....
As literals, another developer will have to read the code to know which literals are valid options and which are not.
As enum, it is still possible to represent each option as a literal, but all the available options are now discoverable.
See also: Literals

## Lean interfaces
If you design your interfaces to be lean, you automatically achieve more discoverable code. By eliminating all the interface pollution, it is easier to get an overview of what remains.
See also: Lean interfaces

## Documentation comments
If you use documentation comments, then another developer can learn more about your API through the IDE's code completion menu, without needing to leave the code they are working on to read through code or documentation.
See also: Documentation

## Naming
Naming is important for discoverability because it's the first piece of information another developer is presented with when they encounter your code or go looking for it.
Type aliases can be used to improve the discoverability of tuples and closures (lambdas). 
Be consistent when naming and follow the naming principles of your programming language.
See also: Naming

## Cohesion
Where you place a piece of code is important to it's discoverability. Do you add a method to the implementation of an existing type, do you place it in the global scope (no), do you extend an existing type or interface, or do you write a new type to contain it. Consider carefully where another developer would expect to find it. Where they would go looking for it.
See also: separation of concerns, single responsibility principle

## Namespacing
Namespacing can be a useful tool for the discoverability of your code, but use it sparingly.

Benefits:
- Reduces the probability of code duplication
- Reduces the learning curve of an api
