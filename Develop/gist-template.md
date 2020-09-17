# Email Regex

This is a tutorial that explains the matching an email regex.

## Summary

The regex will confirm the exact email address of a non-space separated sequence of characters of length greater than one, followed by an @, followed by a sequence of non-spaced characters of length one or more separated by a "." followed by a sequence of non-spaced characters of length two or more. The code is as follows:
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
The components of the regex are the sequences of characters, the brackets which signify matching anything between them, the forward slashes which are the boundaries of the expression, the plus which means to match as many times as possible, the @, the \., the $ which signifies the end, and the {2,6} which means to match at least two times but not more than 6. 

### Anchors
/ regular expression boundary^ represents the beginning of the line or string
$ represents the end of the string, or end of the line

### Quantifiers
{2,6} means to match at least two times but not more than 6

### OR Operator
\. represents a literal period
\  is the regular expression boundary 

### Character Classes
[] the characters listed inside the brackets are part of a matching character set, in this case letters, numbers and characters before and after the @ and letters after the ".".

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
