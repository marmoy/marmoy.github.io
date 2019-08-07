Literals are one of the biggest liabilities in a codebase

- shared reason to change
- high probaility of typos
- runtime errors vs compiletime errors
- not discoverable


## Cohesion
Literals cannot indicate relationships. If one literal is related to another, fx if they are two possible values of an input, then that relationship should be explicitly stated by wrapping them in an enum.

## Literals should be segregated from the rest of the code

## Acceptable literals
There are a few acceptable literals, those that refer to an empty value, fx an empty string or 0 or 1. What literal represents empty depends on the context. Ideally empty should be represented in a different way, such as with nil, but sometimes that is not possibel due to the API, or it's just impractical.



