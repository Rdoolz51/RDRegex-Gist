# What Happens When We Use RegEx To Validate An Email Address?

In this tutorial, I hope to explain the proper usage of the Regular Expression (RegEx) used to validate email addresses.

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
This Regular Expression (RegEx) is used to determine if the email address entered is valid or not.

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
In the expression used for email validation, the anchors use are "^" which represents the start of a string and "$" which represents the end of a string.
### Quantifiers
In the Email Validation Expression there are 2 Quantifiers. The first quantifier we run into is the "+" which means the preceding item, [\da-z\.-] in this case, must appear 1 or more times.
The other quantifier we run into in Email Validation is "{2,6}" which shows how many characters were used in the set. 
### OR Operator
The Email Validation expression does not include any OR operators. But, an OR operator is displayed as "|" when it is used.
### Character Classes
Character classes tell the regex engine to match one of several characters. The characters you want to match are inside of square brackets. In this expression we use:
[a-z0-9_\.-] - lets break this down.
[a-z] - this represents a match if any lowercase letter is found between a-z.
[0-9] - this represents a match if any digit is found between 0-9.
[_] - this represents a match if the "_" character is found.
[\.] - this represents a match if the "." character is found. The "\" character is used to escape the "." so it is taken literally.
[-] - this represents a match if the "-" character is found.
AND
[\da-z\.-] - lets also break this one down.
[\d] - represents that any digit can be used as a match. In the same way we used'0-9'.
[a-z] - this represents a match if any lowercase letter is found between a-z.
[\.] - this represents a match if the "." character is found. The "\" character is used to escape the "." so it is taken literally.
[-] - this represents a match if the "-" character is found.
### Flags
The email validation expression contains no flags. Flags are used following the expression to indicate extra rules, such as "i" which means the whole expressions is case-insensitive. But again, in the case of email validation, we don't use any flags.
### Grouping and Capturing
Groups are determined by '()' In the regex example above ([a-z0-9_.-]+)
'+' show that at least one of the previous tokens must be present to be valid
'[a-z0-9_.-]' show all of the different character classes or tokens that will make this valid for use.
### Bracket Expressions
Bracket expressions group tokens together in order to validate the expression provided.
If I was to validate my own email 'Rdoolz51@aol.com' we can break this down a bit better.
The first bracket '[a-z0-9_.-]' is used to decypher if 'Rdoolz51' is a valid input, which it is.
The '@' is used literally in this expression so it does not need to be in a set of brackets. This just means it's expecting the @ symbol here.
The second braket '[\da-z.-]' is used to determine if 'aol' is a valid input, which again, it is.
"." is used literally in this expression so it does not need to be in a set of brackets. This just means it's expecting the "." symbol here.
The third bracket [a-z.] is used to determine if com is a valid input. Which it is.
### Greedy and Lazy Match
This expression contains 2 greedy operators "{2,6}" and "+". This just means that they will expand the match as far as they can throughout the provided text.
There are no lazy operators in this expression, but they would be indicated using the "?" character.
### Boundaries
There are no boundaries in this expression. Boundaries are represented by the '\b' anchor.
### Back-references
There are no Back references in this expression. Back references are used by '\1' to refer back to a previous section of the expression to use in a later part in the expression.
### Look-ahead and Look-behind
Look ahead and look behind are not used in this expression. Look ahead is used to find characters previous to a key character. Look behind is used to find characters after a key character.
## Author
My name is Ryan Dooley, I am a JavaScript student at CWRU. To find more of my work, check out my GitHub at https://github.com/Rdoolz51
