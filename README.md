# Introduction
`string`s are one of the most commonly used types in programming. Whether they
are used for log messages or for text-based interfaces, knowing how to
manipulate strings is very convenient.
```
first_name = 'John'
last_name = 'Smith'
full_name = first_name + ' ' + last_name
```
We have already seen that `+` can be used to add numbers, but `+` can also be
used with `string`s. `+` will concatenate, or combine, `string`s, simply
attaching them one after another. Notice the `' '` which adds a space between
the `first_name` and `last_name`. Without the `' '`, `full_name` would be
`'JohnSmith'`.

Another common idiom in Python and other languages is to combine numbers and
`string`s. Below is an antipattern, and **will not work.**
```
name = 'Einstein'
# Einstein wasn't always the best at school
grade = 53
summary = name + grade
```
Python will throw an error and crash your program if you do this. The proper way
to concatenate numbers and `string`s is to first convert the number into a
`string` using the `str()` function.
```
name = 'Einstein'
grade = 53
# str(grade) will return '53', a string
summary = name + str(grade)
```
This will work as expected.
> ## Sidebar: Comments
> You probably have noticed the usage of the number sign "#" throughout the
> example code in this tutorial. This is called a *comment* and voids the
> remainder of the line. Comments are used by programmers to describe how a
> piece of confusing code works, why a particular approach was taken, or simply
> to comment on some line of code. Lines with comments are completely ignored by
> Python.
> ```
> # print('This line does nothing at all!')
> ```
> Comments can also be written in docstrings, which allow for multiple lines of
> commentary.
> ```
> '''This is a docstring'''
> '''
> Here is
> a multi-line
> docstring
> '''
> ```
## f-Strings
Another way to combine multiple types of data in a `string` is to use the new
Python feature f-Strings.
> **Note:** f-Strings are only available in Python 3.6 and above.
f-Strings provide an easy syntax to embed other `string`s and types of data
within a `string`.
```
name = 'Einstein'
grade = 53
sentence_summary = f'{name} received a {grade} on the test.'
# 'Einstein received a 53 on the test.' is stored in sentence_summary
```
To use an f-String, simply prepend the `string` with an "f".
# Task
Using both f-Strings and standard concatenation, write a program that will ask
the user for their name and age, and print a sentence about them. The output
should look something like this:
```
What is your name? Einstein
What is your age? 140
Einstein is 140 years old.
```
