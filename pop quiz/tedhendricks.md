### Pop Quiz Answers

Legacy code is code that has been untested.

You should try to condense the code to make it easier to read and understand. You should then begin testing the code to see what is functional. You do not want to remove any code until has been tested, as some of it may be functional and removing it could have unwanted sideffects.

total += 1

*I'm struggling to understand this code and what it currently does.*
```
@items = [{name: "Item Name"}]
for i in 0...(@items.size)
  @items[i][:name]
end
```

The initial test are called unit tests

Flog score represents both code quality and code complexity

True, you should always make small changes and while always checking your tests after each change

False, a high flog score is good
