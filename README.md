# Regex Tutorial

This Regex Tutorial is created to help you understand the sequence of special characters used in Regex expressions. These expressions are used to verify whether a pattern matches a frequently used regular expression, such as an email, a URL link, for numerical digits, password strength, usernames, dates, time format and more. 

## Summary

This tutorial will focus on matching an email with the following:

<pre>/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/</pre>

The regular expression will start with at least 1 characters from `A-Z`, `0-9`, `_`, `.` and `-`, followed by `@` then at least 1 character from the same set then `.`, and finally at least 2 to a maximum of 6 alphanumeric characters to end the expression. 


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

A regular expression is a sequence of characters that define a search pattern for text. They are composed of the below components which 

### Anchors

`/^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$/`
<br>

Line anchors define the starting and ending characters of an expression. The syntax used are `^` and `$` respectively. 
<hr>

### Quantifiers

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

Quantifiers specify how many times a character or group of characters must appear in the expression for a match to be found.

| Quantifier  | Description |
| ------------- | ------------- |
| `*`  | matches 0 or more times  |
| `+`  | matches 1 or more times  |
| `?`  | matches 0 or 1 time  |
| `{n}`  | matches n times  |
| `{n,}`  | matches at least n times  |
| `{n,m}`  | matches from n to m times  |

In the email regular expression we have `+` and `{2,6}`. The `+` suggest that at least 1 of the specified character must be present and similarly `{2,6}` indicate that at least 2 and a max of 6 times of the specified characters must be present.\
<hr>

### Grouping Constructs
/^`([a-z0-9_\.-]+)`@`([\da-z\.-]+)`\.`([a-z\.]{2,6})`$/

A grouping construct is a set of sub-patterns written inside parentheses `()`
<hr>

### Bracket Expressions
/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

A bracket expression, denoted by square brackets `[]` is used to match a specific set of characters classes. It symbolises the beginning of a character class or quantifier expression. 
<hr>

### Character Classes

/^([`a-z0-9_\.-`]+)@([`\da-z\.-`]+)\.([`a-z\.`]{2,6})$/

Character classes is used to determine what character are expected in the regular expression.
I.e. `a-z0-9_` allows for characters `A-Z`, `0-9` and `_`.

In addition, there are more generalised character classes defined below:

| character classes | Description |
| ------------- | ------------- |
| `/d`  | matches a single digit  |
| `/w`  | matches a word  |
| `/s`  | matches a space character (includes tab and line breaks)  |
| `.`  | matches any characters  |

I.e. `\da-z\.-` will match a single character `A-Z`, `0-9`, `.` or `-`.

<hr>

### The OR Operator

The OR Operator within a regular expression is used to indicate either one of our components. It is represented by `|` and separates the expressions. An example is shown:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`|`\w+[\+\.\w-]*@([\w-]+\.)*\w+[\w-]*\.([a-z]{2,4}|\d+)$/

Both of the components are valid regular expressions for email addresses.
<hr>

### Flags
Flags are used to modify the output of a regular expression, hence also called modifiers. 
| Flag  | Description |
| ------------- | ------------- |
| `i`  | Case Insensitive: Match lower and upper case.  |
| `g`  | Global Search: Looks for all matches, not just the first. |
| `m`  | Multiline: Anchor and enables multiline mode for test string |
<hr>

### Character Escapes
/^([a-z0-9_`\`.-]+)@([\da-z`\`.-]+)\.([a-z`\`.]{2,6})$/

A backslash `\` is used to escape that grouping and is used when any of the special characters is used in the string. 

Example: `([a-z0-9_\.-]+)` will allow this grouping to contain A-Z, 0-9, _ and `.` `-` which normally would be considered as special casing. 

<hr>

## Author

This tutorial is created by Kevin Peng. [Github](https://github.com/cn-kp)

