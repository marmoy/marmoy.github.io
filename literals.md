# Literals

## What are literals
Literals are any non-named value. Common literals are string literals, fx ´"some string literal"´, number literals, fx ´2´, ´3.14´

Literals are one of the biggest liabilities in a codebase
- high probaility of typos
- runtime errors vs compiletime errors
- not discoverable
- they are susceptible to implicit replationships, fx a shared reason to change. , making it easy to forget to change the values of all when one is updated.

## Cohesion
Literals cannot indicate relationships. If a set of literals are related to another, fx if they are possible values of an input or keys to a json dictionary, then that relationship should be explicitly stated, in the first case by wrapping them in an enum, in the second case by making them static constants in a shared namespace (enum/struct/class)

## Getting rid of literals
There will always be literals in a codebase. The important thing is to segregate them from the rest of the code, so that they are gathered in cohesive groups. Another important aspect of removing literals from the code is to recognise when several literals represent the same thing. That could be several placholder texts, which will always have the same value, even if that value should change in the future. If several literals have the same value and the same reason to change, then they should all be replaced by a single constant and referenced instead. The constant should be placed in a context and scope that can be referenced from all relevant places, without being global. It may turn out to be necessary to inject the constant.

See also:
- Dependency injection
- Scope

## Acceptable literals
There are a few acceptable literals, those that refer to an empty value, fx an empty string or 0 or 1. What literal represents empty depends on the context. Ideally empty should be represented in a different way, such as with nil, but sometimes that is not possible due to the API being used, or it's just impractical.



