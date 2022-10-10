# Matching an Email

This tutorial will break down a regex (regular expression) that finds all emails in a text. 


## Summary

In each section below, you will be able to see different parts of a regex. Each part in the algorithim has a specific role in allowing a user to locate all emails in a text. 

We will be evaluating and analyzing the following Regex algorithim:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
Anchor: ^ $ (start and end)
Note these examples are found in the beginning and end of the code string. 
 Anchors assert that the engine's current position in the string matches a well-determined location: for instance, the beginning of the string, or the end of a line.

### Quantifiers
Quantifiers found in code snippet: + and {2,6}
Quantifiers indicate numbers of characters or expressions to match.
Quantifier examples: *, +, ?, { n } {n, } {n, m}
In our code snippet, the + is used to say "and" or "followed by". 
In the example, group one is followed by group two which is followed by group three. 
The {2,6} bracket says to look for any group that are 2-5 characters long. It is shown in the 3rd group of the algorithm which says to look for any group of letters or dots that 2-5 characters long to account for region-specific top level domains such as .com, .net as examples. 

### Grouping and Capturing / Bracket Expressions
In this section, I will combine both of these Regex types as they are used together to create groups of values and strings of characters. 
Code Snippet: ([])
The brackets identify the string of values in this grouped character class created by parentheses. 
In this case, there are 3 grouped strings of characters. 

Group 1: ([a-z0-9_\.-]+) - We match one or more lowercase letters between a-z, numbers between 0-9, underscores, periods, and hyphens. 
Group 2: ([\da-z\.-]+) is followed by the @ symbol. The domain name must be matched which can use one or more digits, letters between a-z, periods, and hyphens. 
Group 3: ([a-z\.]{2,6}) follows the period behind the domain name in the previous group. This 3rd group matches the top level domain. This group will look for any group of letters or dots that are 2-5 characters long. 


## Author

Samantha Karpovck created this gist page to breakdown a regex for matching an email. Please checkout my github for any other projects I've created and collaborated on. 
Github: https://github.com/samkarp700
