# Unexpected Behavior When Directly Modifying Instance Variables in Ruby

This example demonstrates a potential issue in Ruby when instance variables are modified directly from outside the class using `instance_variable_set`. While functional, this approach undermines encapsulation and can introduce subtle bugs.

## Problem
The `MyClass` example shows how altering `@value` externally bypasses the class's intended methods.  This makes the code harder to debug and maintain as the state of the object becomes less predictable.

## Solution
Always use accessor methods (getters and setters) to interact with an object's internal state. This ensures controlled modification, allowing for validation or additional logic within the class.

## Recommended Practices
- Favor using accessor methods (`attr_accessor`, `attr_reader`, `attr_writer`).
- Keep instance variable access within the class's methods to maintain encapsulation and predictability.