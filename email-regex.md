# Email Regex Tutorial

A regex (regular expression) is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regex can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. 

This tutorial will go over the regex pattern associated with an email address.

## Summary
````
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
````
The following code above is the regex format for an email address. The following sections will break down the different parts of this expression to decode/figure out how this particular regex matches email addresses.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
````
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
````
In the following regex, there are two positioning anchors: `^` and `$`
- `^`: States the beginning of string/line
- `$`: States the end of string/line

### Quantifiers
````
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
````
In the following regex, there are two different quantifiers: `+` and `{n,m}`
- `+`: has character that matches 1 or more times
- `{n,m}`: has character that matches from n to m times

So in this case, the email regex is looking for an expression that has at least 1 character before the literal @ sign `/^([a-z0-9_\.-]+)`, at least one character after the @ sign but before the literal period (`\.`) `[\da-z\.-]+)`, and has 2-6 characters after the literal period `([a-z\.]{2,6})`

### Grouping and Capturing
````
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
````
From this expression, the group `[a-z0-9_\.-]+)` captures the **user email name**, the group `[\da-z\.-]+)` captures the **email service**, and the group `([a-z\.]{2,6})` captures the **top level domains** (.com, .net, etc.)

### Bracket Expressions

The bracket expressions lets us know what characters are included in the search

- `[a-z0-9_\.-]`: states that the search can include lowercase letters `a-z`, numbers `0-9`, underscore `_`, backslash `\`, period `.`, and hyphens `-`

- `[\da-z\.-]`: states that the search can include decimal digits from 0-9 `\d`, lowercase letters `a-z`, backslash `\`, period `.`, and hyphens `-`

- `[a-z\.]`: states that the search can include lowercase letters `a-z`, backslash `\`, and period `.`

## Author

Vivian Chen
www.github.com/vivianc11
