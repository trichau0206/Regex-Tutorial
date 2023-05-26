# Title (Regex)

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

### Anchors
Anchors are used to specify the position of a pattern within the text being matched. The two most common anchors used in regular expressions are ^ (the Caret symbol) and $ (the Dollar sign). The Caret symbol is used to match the beginning of a line, and the Dollar sign is used to match the end of a line.
### Quantifiers
Quantifies specify how many time a preceding element should occur in the text being matched. There are many quantifiers that you can use:

* The asterisk is used to match zero or more occurrences of the preceding element
+ The plus sign is used to match one of more occurrences of the preceding element
? The question mark is used to match zero or one occurrences of the preceding element
{n} Curly braces are used to specify an exact number of the occurrences of the preceding element
{n,} Curly braces with a comma are used to specify a minumum number of occurrences of a preceding element
{n,m} Curly braces with a comma between two values is used to specify a range of occurrences of a preceding element
### Grouping Constructs
Capturing group () - Groups together elements and also captures and remembers matched text for later use, referenced or retrieved using backreferences
Non Capturing group (?: ) - Similar to capturing groups as in they group together elements, but they do not capture or remember the matched text. Useful when needing to apply operations to a group of elements but do not need to reference them later.
### Bracket Expressions
In this example ([a-z0-9_\.-]+) is a bracket expression that matches one or more lower case letters, digits, underscores, dots or hyphens in the username part of an email address. This expression ([a-z\.]{2,6}) matches exactly 2 to 6 lowercase letters of dots, which represent the top-level domain (TLD) part of an email address
### Character Classes
Character Classes are enclosed in [] in regex and define a set of characters that can match a single character in the input text.

@ Matches the "@" symbol, and \. matches a dot character
[a-z0-9_\.-] Matches any lowercase letter a-z, digits 0-9, underscore, dot or hyphen
[\da-z\.-] Matches any digit, lowercase letter, dot or hyphen
[a-z\.] Matches any lowercase letter or dot
### The OR Operator
The OR operator in regular expressions is denoted by the vertical bar | and allows for matching either one pattern or another. In the given regular expression, the OR operator is used in the character class ([a-z\.]{2,6}) to allow for matching either lowercase letters (a to z) or dots (.), and the quantifier {2,6} specifies that there must be between 2 to 6 occurrences of the preceding pattern (i.e., lowercase letters or dots). 
### Flags
This particular example does not contain any flags, however flags are optional parameters that modify the behavior of the regex pattern matching. They are typically added after the closing delimiter of the regular expression and are used to specify options such as case-insensitivity, global matching, multi-line mode, etc. Examples of common flags include i for case-insensitive matching, g for global matching, and m for multi-line mode.
### Character Escapes
Character escapes are special sequences of characters that have a specific meaning in regular expressions. In this regex, the following character escapes are used:

\d - Represents a digit character (0-9).
. - Represents a period character. However, it is not used as a character escape in this regex, but as a literal period character, as it is not preceded by a backslash
## Author

This Regex Gist was written by Tri Chau for the UC Berkeley EDX Full-Stack Cohort. [link](https://github.com/trichau0206)
