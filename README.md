# Regex Tutorial

This guide to Regex (regular expressions) will explain what Regex is, as well as how it can be used in your code.

## Summary

A reguar expression is a sequence of characters that defines a search pattern in text. One way that it can be used in coding is for validating user input. In this tutorial we will be breaking down a regex that matches an email address:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping and Capturing](#grouping-and-capturing)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
---
### Anchors
There are two types of anchors:
 ```
 ^
 ```
 This indicates that the string we are matching should start with whatever is written after that anchor. In our example, we are indicating that the string should start with either of the characters valid for an email address: ```/^([a-z0-9_\.-]+)```
 ```
 $
 ```
 This indicates that the string we are matching should end with whatever is written before that anchor. In our example, we are indicating that the string should end with either of the characters valid for an email address: ```([a-z\.]{2,6})$/```

---
### Quantifiers
A quantifier is appended to a character (or a character class, or a [...] set etc) and specifies how many we need.
There are four types of quantifiers:
```
*
```
This means that the last character before this quantifier can appear zero, one, or many times consecutively in the string. We do not have this quantifier in our email matching regex.
```
+
```
This means that the last character before this quantifier has to appear at least once or more times consecutively in the string. In our example we are indicating that there cannot be an empty string before the @ sign by placing the ```+``` quantifier, meaning at least one of these characters that we are allowing has to be appear ```/^([a-z0-9_\.-]+)``` and we are doing the same thing after the @ sign ```([\da-z\.-]+)```
```
?
```
This means that the last character before this quantifier cannot be there or can appear just once in the string. We do not have this quantifier in our email matching regex.
```
{n}
```
This means that the last character before this quantifier must appear n times in the string. We do not have this quantifier in our email matching regex.

---
### Grouping and Capturing
```
()
```
Parentheses create a capturing group with the value inside of them. In our email matching regex, we are using parentheses here ```([a-z0-9_\.-]+)```, ```([\da-z\.-]+)```, ```([a-z\.]{2,6})$/``` to capture all of the characters that we specified inside of the parentheses.

---
### Bracket Expressions
```
[]
```
In our email matching regex we are using brackets here ```[a-z0-9_\.-]``` to specify that we are looking for any letter from a to z, as well as any number from 0 to 9.

## Author
Written by Saidana. Click [here](https://github.com/smillkaa) to see the author's Github profile.