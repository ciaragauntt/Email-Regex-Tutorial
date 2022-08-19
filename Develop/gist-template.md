# Matching an Email Regex Tutorial

If you have found this repository, you must be wondering what a regex is and specifically how to match an email
using regex. To begin lets start simple and define what regex means. Regex stands for "Regular Expression".
These regular expressions are a series of special characters that help define a search pattern. If a user
inputs something specific that we want to sift through or give parameters, we will use a regular expression.

## Summary

Today we will be learning all about the regex used to matching an email. Lets say you create a website and 
want the user to input their email address to log in. Once someone enters an email address you want to be 
able to validate that the email address has the correct components before trying to send an email to it.
It would be a useless form if a user put in am email without a ".com" at the end for example. Basically
we want the user to run into as little the amount of problems as possible. And of course we want the 
website to run as smoothly as possible. Below you will see the regex for matching an email address...
then we will break it down throughout the tutorial.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors are super important in regular expressions matching a position before or after characters. In this 
regex we use the anchors ^ and $.

^ : the beginning of the email adress
$ : the end of the email address

### Quantifiers
Quantifiers in regular expressions help specify how many instances of a character, group, or character class
must be present. The quantifiers in the email regex is + and {2,6}.

+ : shows that there is another sequence to be matched 
{2,6} : specifies that the input should be at least 2 characters and a maximum of 6 characters. 

## OR Operator
There is not an OR Operator in the email regax, but I will explain it anyway. OR Operators are used to match one of multiple
patterns such as this OR that. An example would be hi|hello. 

### Character Classes
Character classes are used to tell the regex engine to match only one out of several characters. This helps the 
engine find a word even if it is misspelled or written in another language. The character classes in the email regex 
are inside the brackets.

a-z : telling the regex engine letters a-z inclusive in lower case
0-9 : telling the regex engine that numbers 0-9 are inclusive 
_ : telling the regex engine that you can use an underscore
\. : telling the regex engine that you can use a "."

### Flags
There are no flags in this expression, but I will explain what they are anyway. Flags are components of the expression that
affect the search. Below are a list of the flags that can be used and their specific function.

i : this flag states that the search is case insensitive; meaning there is no difference between "a" and "A".
g : this flag states that the search looks for all matches, without it only the first match is returned.
m : this flag states that it is a multiline code
s : this flag enables the "dotall" mode that allows a "." to match a newline character.
u : this flag enables unicode support and correct processing of surrogate pairs.
y : this flag enables "sticky" mode where is will search at the exact position of the text.

### Grouping and Capturing
A group in a regex ecpression is anything that is enclosed in parantheses. Grouping is used to create blocks of patterns
so you can add other modifiers to them as a singular or as a whole. The email regex uses grouping at ([a-z0-9_\.-]+) and
([\da-z\.-]+) and ([a-z\.]{2,6}).

 ([a-z0-9_\.-]+) : matches the users email name
 ([\da-z\.-]+) : matches the email service being used
 ([a-z\.]{2,6}) : captures the ".com"

### Bracket Expressions
Brackets indicate a set of characters to match. Each individiual character in the brackets will match. Bracket
expressions used in the email regax are [a-z0-9_\.-] and [\da-z\.-] and [a-z\.] .

[a-z0-9_\.-] : matching letters a-z is case sensitive while also matching characters 0-9, _ , and -
[\da-z\.-] : matching a single digit from 0-9, any character a-z case sensitive, and characters "." and "-"
[a-z\.] : matchigng the characters a-z case sensitive and the character "."

### Greedy and Lazy Match
Greedy means the longest possible string while lazy means the shortest possible string. 

+ : greedy quantifier will match as many times as possible 
{} : greedy quanitifier matching 2,6 for the last capture group

### Boundaries
There are no boundaries in this expression, but I will still give a short explanation. There are three different positions 
that qualify as a word boundary"
* Before the first character in a string, if the first character is a word
* After the last character in the string, if the last character is a word
* Between two characters in a string, where one character is a word and the other is not 

### Back-references
There are no back references in this expression but I will explain briefly. Back references that refer to the previous 
part of the matched regular expression. Back references are stated with a backslash and a number. Ex. \1

### Look-ahead and Look-behind
There are no look ahead or look behinds in this expression, but I will briefly explain it. Lookahead allows you to add 
a condition to what follows while look behind does the oposite and allows you to add a condition to what is happening previouly.

## Author

Hello! My name is Ciara and I am currently a student at the University of Utah enrolled in the Trilogy coding bootcamp.
I will be graduating in October, so make sure to keep a lookout for more repositories on my github!

Github: https://github.com/ciaragauntt

