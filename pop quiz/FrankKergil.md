What is Michael Feathers definition of "legacy code"?
Legacy code is source code that relates to a no-longer supported or manufactured operating system or other computer technology.

What is the first thing you should do when refactoring legacy code?
The first thing you should do is to run a test to see what specifically is depreciated about the code.

How would you refactor this code?

1.

total = total + 1   
total += 1

2.

@items = [{name: "Item Name"}]
for i in 0..(@items.size-1)
  @items[i][:name]
end
 
[{name: "Item Name"}].each { |hash| hash[:name] }
 
What do you call the initial tests created by Randy?

a. Characterization Tests

b. Unit tests

c. Feature tests
```
d. Integration tests
```
What does Flog score represent?

a. Code quality
```
b. Code complexity
```
c. none of the above

d. both A, B

```True``` / False - You should always make small changes and while always checking your tests after each change.

True / ```False``` - A high flog score is good
