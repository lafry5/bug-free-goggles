# Email Regex

This is a tutorial that explains the regex for matching an email.

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
The components of the regex are the sequences of characters, the brackets which signify matching anything between them, the forward slashes which are the boundaries of the expression, the plus which means to match as many times as possible, the @, the \., the $ which signifies the end, and the {2,6} (quanitifer) which means to match at least two times but not more than 6. 

### Anchors
The / regular expression boundary represents the beginning and end of the line or string. The ^ represents the beginning of the string or beginning of the line. The $ represents the end of the string or the end of the line.

### Quantifiers
Quantifiers indicate numbers of characters or expressions to match. In the matching an email regex, {2,6} means to match the characters prior to it at least two times but not more than 6 times.

### OR Operator
The operator backslash period represents a literal period (as seen above between the two capture groups and inside the last capture group).


### Character Classes
The characters listed inside the brackets [] are part of a matching character set, in this case letters, numbers and characters before and after the @ and letters after the ".". What it means is to match what is inside the []. In the instance of the first and second brackets, since there is a + afterwards, that means to match the letters, numbers and characters as many times as possible. 

The . is used in the expression in two instances to represent any character. The instances are inside the capture groups in parenthesis.

### Flags
Flags are identified at the end of the slash character to specify details about executing the expression. For example an i after the slash (i.e. "/i") represents insensitive and makes the whole expression case-insensitive...for instance /aBc/i would match AbC. There are no flags identified at the end of the regex expression for matching an email.  

### Grouping and Capturing
A capture group is a section of a regular expression enclosed in parentheses. The first capture group is [a-z0-9_\.-]+ , the second capture group is [\da-z\.-]+ and the third capture group is [a-z\.]{2,6}

### Bracket Expressions
The first bracket expression is [a-z0-9_\.-]. This represents letters a through z, numbers 0 through 9 and characters -, \, any character, and -.  The second bracket expression is [\da-z\.-]. This represents any digit, letters a through z, \, any character, and -. The third expression is [a-z\.], which is a through a and a ".".

### Greedy and Lazy Match
This regex is not using a lazy quantifier. Quanitifers by their nature are greedy since they are trying to match the largest number of strings as possible. (See quanitifers above.) 

### Boundaries
A word boundary \b is a test, just like the anchors ^ and $. When the regexp engine comes across \b it checks that the position in the string is a word boundary (at string start, between two string characters, at string end). In this regex expression there are no defined word boundaries.

### Back-references
Backreferences match the same text as previously matched by a capture group. For example, let's say there is another section in the regex that matches the first capture group i.e. [a-z0-9_\.-]+. Instead of re-writing that again later in the expression, instead, all you need to do is put \1 (backslash one) to reference the first capture group. \1 represents matching the exact same text that was in the first capture group. However, there are no back-references in this regex to reference previous capture groups so there are no back-references.

### Look-ahead and Look-behind
Look-ahead and look-behind are collectively called look-arounds. These are zero length assertions, just like the start and end of a line and word anchors. 
For Look-ahead the syntax is: X(?=Y), it means "look for X, but match only if followed by Y". There may be any pattern instead of X and Y. Look-ahead allows to add a condition for “what follows”. For the look-behind: (?<=Y)X, matches X, but only if there’s Y before it. In the case of the matching email regex there are no uses of the look-ahead or look-behind.

## Author

The author has been a technical project manager for 15 years. She received her Bachelors in Mathematics from the University of Pittsburgh, a Masters in Electrical Engineering from USC and an MBA from the University of Phoenix. She is currently attending the University of Arizona  bootcamp for Full Stack Web Development.

[Laura's GitHub profile](https://github.com/lafry5)
