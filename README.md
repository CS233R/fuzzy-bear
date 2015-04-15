# Intro to Ruby

### Running a ruby program in the console or in 'irb'

#### *Regular console example*

To run a ruby ruby program on your computer all you need to do is type ``ruby path/to/your/ruby/program.rb``. If you want to minimize typing you can first change into the directory that the file is in by typing ``cd path/to/directory`` and then you can just type ``ruby program_name.rb``

#### *irb example*

To test a bit of ruby code anywhere on your computer just type ``irb`` in the console. This will open up an interactive ruby environment where you can write any ruby code that you desire.

> Note that any variables that you declare in your 'irb' session will only be available to that session. Once you type ``quit`` to exit the 'irb' session all of your declared variables will be discarded

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
