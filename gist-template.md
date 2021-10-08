# How To Match A Hex Value Using A Regular Expression

In this tutorial, I'll explain How To Match A Hex Value Using A Regular Expression.
Instead of searching through a document for hex values, you can use this regular expression to do the work for oyu. 

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

Here is the code snippet of the regular expression that you'll use to identify hex values:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

### This regular expression consists of a few main parts:

#### 1. Start with a '#' sign, but make it optional:

`/^#?`

#### 2. Match a single character in the alphabetical range a-f, or numerical range 0-9

`[a-f0-9]`

#### 3. Match the previous character set 6 times:

`{6}`

#### 4. OR:

`|`

#### 5. 


`[a-f0-9]`


#### 6. Match the previous character set 3 times: 


`{3}`


#### 7. End the regular expression

`$/`


#### Note:

The section of the regular expression enclosed in the (), separated by the '|' represents the logic of the OR statement.

`('THIS'|'THAT')`

#### BONUS: 
To make this regular expression case insensitive, add an additional range to the character classes, or add the 'i' flag to the end of the pattern. Either of these will perform a case insensitive search:


`/^#?([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$/`

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/i`

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

Anchors are Regex components that don't match characters.
Instead, they explain something about the string or matching process. Here is a list of Regex anchors: 

- ^: Beginning of string (or line, depending on the mode)
- $: End of string (or line, depending on the mode)

Source: http://www.rexegg.com/regex-anchors.html


### Quantifiers

Quantifers go after an instance of a character or group, and define how many times you should match this character/group in your search.

Quantifiers can be either "lazy" or "greedy". 

Lazy: Match as many occurences of a pattern as possible

Greedy: Match as few occurrences of a pattern as possible.

| Greedy quantifier  | Lazy quantifier | Description |
| ------------------ | --------------- | ----------- |
| * | *? | Match zero or more times. |
| + | +? | Match one or more times. |
| ? | ?? | 	Match zero or one time. |
| { n } | { n }? | 	Match exactly n times. |
| { n ,} | { n ,}? | Match at least n times. |
| { n , m } | { n , m }? | Match from n to m times. |

Source: https://docs.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions

### OR Operator

The "OR" operator is denoted by the pipe character: " | ". 

When using the OR operator, you are defining two potential matches for your search:

'THIS' or 'THAT'.

OR conditions must be contained within parenthesis, and your regular expression will resemble this: 

`('THIS'|'THAT')`

Source: https://www.ocpsoft.org/tutorials/regular-expressions/or-in-regex/


### Character Classes

Character classes, or character sets match one character. They are defined withing square brackets, and can also match a range of characters. Character classes are case sensitive. Here are a few examples:

`[zack]` matches 'zack' in the doucument.

`[a-z]` matches one character that can be any lowercase alphabetical character

`[A-Z]` matches one character that can be any uppercase alphabetical character

`[0-9]` matches one character that can be any numbers

`[a-zA-Z]` matches any word that starts with any character, upper or lowercase, that ends with 'ack'. 

### Flags

Flags are added at the end of your pattern, and can be combined for more specific searches. 

| Flag | Description |
| -----| ----------- |
| d | Generate indices for substring matches |
| g | Global search |
| i | Case-insensitive search |
| m | Multi-line search |
| s | Allows . to match newline characters |
| u | "unicode"; treat a pattern as a sequence of unicode code points |
| y | Perform a "sticky" search that matches starting at the current position in the target string |

For example, the following pattern will perform a case-insensitive search:

`/pattern/i`


Source: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions#advanced_searching_with_flags


### Grouping and Capturing

Use parenthesis to group a specific part of a regular expression. This allows you to apply other regex components like quantifiers and or statements. 

For example, the following regular expression will search for 'xyzxyz'. The group is contained within the parenthesis, and the quantifier searches for the grouped pattern twice. 

`(xyz){2}`

Source: https://www.regular-expressions.info/brackets.html

### Bracket Expressions

Square brackets are used to match a single character.

See the section above on [Character Classes](#character-classes) for more information. 

### Greedy and Lazy Match

Lazy: Match as many occurences of a pattern as possible

Greedy: Match as few occurrences of a pattern as possible.

See the section above on [Quantifiers](#quantifiers) for more information. 

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

My name is Zack Miller and I am a student at [Rutgers Coding Bootcamp](https://bootcamp.rutgers.edu/coding/). 

Follow me on [github](https://github.com/zacktmiller92):

https://github.com/zacktmiller92
