# Let's Learn REGEX!

Hello! Today I'll show you a brief document to walk you through Regex, as well as it's various purposes. I hope you can learn something! That said let's just hop right into it.

## Summary

Regex, also known as "Regular Expression" is a format of rational statement that can be used to categorize and sort data. This is useful for setting parameters for a secure password, as well as for searching a document for referances within a specific framework. An example of a Regex expression is /([A-Z])/ this represents anything using the character set of the capitalized alphebet, from this a computer could verify that a password only had A-Z characters, or a search program could find anything that consisted only of capital A-Z.

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
Anchors are the part of Regex that handle specific characters being at specific points. The ^ for example ensures the following character sets apply to the first character and no other character. If you need to have the first letter always be capitol, this is the expression you would use to ensure that. Likewise, $ applies to the end of a statement, you would use this if you need a password to end with a number for example.

### Quantifiers
Quantifiers give a limit to how many times a character can be used. The * quantifier may be familiar, because it is normally used to select all in various programs. In Regex, * allows you to let this apply to anything, specifically 0 or greater. + and ? on the other hand can only be used to match 1 or more, or zero or 1 times respectively. For more specific formatting we need curly brackets. {x} lists the precise amount of matches needed, {x ,} matches at least x times, and {x, y} states a minimum and maximum number of occurances.

### Greedy and Lazy Match
There are also "lazy" versions of operators, which to my understanding means that it applies to every individual selected body instead of the entire document.

### OR Operator
The or operator is just a | that can be used to divide words or expressions. For example you could type /([A-Z])/ or /([1-9])/ as /([A-Z | 1-9])/. Thhis can divide specific combinations of letters as well.

### Character Classes
Character classes are used to identify a set of characters, this can be done by either listing characters or defining a range. If you wanted to define a range A through Z for example, you would put [A-Z]. This can also be used on a smaller scale, if you wanted to have either "gif" or "jif" accepted as a spelling you could write [jg]if and the Regex would accept either. The inverse of this can be done by adding a carrot after the first bracket. [^A-Z] would exclude anything capitol A through capitol G. 

### Flags
A regular expression is defined with two slashes, characters that come after that are "flags."  The i flag tells us things are case insensitive, the g flag tells the program to look for more than 1 match, m enters multiline mode, s enters dotall mode, u enables unicode support and y enters sticky mode.

### Grouping and Capturing
Grouping is the act of putting a group of characters in parenthesis, the text inside them can have operators attached to them. For example, (123){3} can apply to 123123123 while (123) can apply to 123. 

### Bracket Expressions
Bracket expressions are a character class that matches one character with a set of character. Both this and regular classes use square brackets as syntax. 

### Boundaries
The syntax to set a boundry is /b. /b example /b would accept anything that is "example" but not example123 for example. Boundaries allow you to select things that aren't part of a larger word.

### Look-ahead and Look-behind
Lookaround assertions allow you to alter what is around a certian character in an expression. Syntactically you use "character"(?!"unwantedchar") to disable a certain character from coming after a specified character. Inversly, to ensure a character has to come after another, you would use Char(?=wantedChar) and that would ensure wantedChar comes after Char.

## Author

My name is Ronan Smith https://github.com/RonanSilasSmith