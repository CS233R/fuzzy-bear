# Intro to Ruby

### Running a ruby program in the console or in 'irb'

#### *Regular console example*

To run a ruby ruby program on your computer all you need to do is type ``ruby path/to/your/ruby/program.rb``. If you want to minimize typing you can first change into the directory that the file is in by typing ``cd path/to/directory`` and then you can just type ``ruby program_name.rb``

#### *irb example*

To test a bit of ruby code anywhere on your computer just type ``irb`` in the console. This will open up an interactive ruby environment where you can write any ruby code that you desire.

> Note that any variables that you declare in your 'irb' session will only be available to that session. Once you type ``quit`` to exit the 'irb' session all of your declared variables will be discarded

### Set and get variables

#### *Setting variables*

To declare and initialize a variable simply type ``variable_name = value``. If the value is a string then enclose the value in single quotes.

*Example*
```ruby
name = 'Ted Hendricks'
age = 22
```

#### *Getting user input*

Use the **gets** method to store user input into a variable. To do this initialize the variable to the value *gets* ``variable_name = gets``.

#### *Displaying variables*

Use the **puts** method to display output.

*Example*
```ruby
greeting = 'Hello '           (store a string variable)
puts 'What is your name?'     (output)
name = gets                   (requires input)
puts greeting + name          (outputs both)
```
*Output*
```
What is your name?            (output)
Ted Hendricks                 (input)
Hello Ted Hendricks           (output)
```

# Learning examples and explanations
``Jules, Ted, Ashley, Frank``

## Strings
### String Methods

---

#### String alinging with ``.ljust`` ``.rjust`` & ``.center``

For string formatting you have three main options that are almost identical to what you would see in a Microsoft Word document.

- Left align ``.ljust``
- Right align ``.rjust``
- Center ``.center``

#### Aligning examples
*Recipe*

```ruby
<string>.ljust(<int> [, <optional_seperator>])
<string>.rjust(<int> [, <optional_seperator>])
<string>.center(<int> [, <optional_seperator>])
```

*Example*

```ruby
"mississippi".ljust(20, "-")	=>	'mississippi---------'
"mississippi".rjust(20, "-")	=>	'---------mississippi'
"mississippi".center(20, "-")	=>	'----mississippi-----'
```

> Notice that the center alignment puts the extra separator on the right end of the string

---

#### String substitution with ``.tr`` & ``.tr_s``

``.tr`` and ``.tr_s`` function similarly to ``.gsub`` in the idea that they either replace text with other text or remove some sort of text. It is hard to describe in english so lets see an example

*Recipe*

```ruby
<string>.tr(<string>, <replacement_string>)
<string>.tr_s(<string>, <replacement_string>)
```

*Example*

```ruby
"mississippi".tr("sp", "Y") 	=> "miYYiYYiYYi"
"mississippi".tr_s("sp", "Y") 	=> "miYiYiYi"
```

> ``.tr`` replaces every character passed in the first argument one-for-one with the replacement string.
> ``.tr_s`` replaces every character passed in the first with only one of the replacement string

---

#### String Interpolation

String interpolation allows for a variable to be entered into a string, provided the correct syntax is used. In order for interpolation to be used, you need to use " ". For example:
    
   ```ruby
puts "Hello, what is your name ?"
name = gets
puts "Welcome #{name} "
```
Since we are using the double quotes, the name the user types in will be in the string. Using ' ', however, will give a different result:

```ruby
puts "Hello, what is your name ?"
name = gets
puts 'Welcome #{name} '
```
 The output you get from this will be Welcome #{name}. As you can see, it is important to use the double quotes if you want a  variable to be included into a string.        

Another way in which interpolation can be used is either %Q or %q. Using these, %Q is the same as " ", while %q is the same as ' '. 

> Using %Q or %q are preferable in large blocks of code because when you are enclosing your code, you
> can use any delimiter to enclose it and not have to continuously use quotes.


#### Capitalize -> new_str

When you use .capitalize at the end of a str it returns a copy of the string with the first character uppercased and the rest of the characters lowercased. 

```ruby
"hello".capitalize => "Hello"
"HELLO".capitalize => "Hello"
"123ABC".capitalize => "123abc"
```

#### Capitalize! -> str or nil

When you use .capitalize! at the end of a str, it will also return a copy of the string with the first character uppercased and the rest of the characters lowercased. But it will return nil if there have been no changes made.

```ruby
a = "hello"
a.capitalize! => "Hello"
a => "Hello"
a.capitalize! => nil
```
