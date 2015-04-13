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