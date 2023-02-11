# Regex Tutorial
This is a tutorial on how a regex works. A regex, or a regular expression, is a sequence of characters that specify a distinct search pattern. When utilized in code or algorithms, a regex can be used to find patterns within a string, find and replace characters in a string, or even to validate inputs.

## Summary
A Hex Value is a hexidecimal value used to reference colors, commonly used in coding. It is a 6 symbol code made of three different 2 symbol elements. Each of the 2 symbol elements represents a color value from 0 to 255, and the symbols can be letters or numbers. There is standard Hexidecimal code (6 characters) and shorthand Hexidecimal code (3 characters) For today's regex tutorial, we will be breaking down the components of a regex used to match a Hex Value:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
`/^`#?([a-f0-9]{6}|[a-f0-9]{3})`$/`

We use the `^` anchor when we are trying to read the beginning of a string in a component. 
Additionally, we use the `$` anchor when we are trying to read a string in which the $ signifies the end of the string, using the characters preceding. In the regex above, everything in between `^` and `$` is being utilized to identify a pattern.

### Quantifiers
/^#`?`([a-f0-9]`{6}`|[a-f0-9]`{3}`)$/
Quantifiers are used to set limits on the string the regex is trying to match to. They are greedy operators, which means that they match as many occurences of a specific pattern as many times as possible (we will discuss a lazy operator later). In the above regex, `?` matches the pattern zero times or once. `{}` can be used in different ways to set limits, but in this example `{n}` signifies that the pattern is matched exactly n number of times (`{3}`,`{6}`).

### OR Operator
/^#?([a-f0-9]{6}`|`[a-f0-9]{3})$/
Operators are used to expand upon parameters in a regex. They allow us to group two different contructs together under one search engine. The OR Operator `|` requires that the string that matches only has to match one of the constructs in order to pass. This is paired with a lazy operator to ensure the most broad amount of matches.

### Character Classes
/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/
A character class defines a set of characters in a regex that can be used as a match for a string. One type of character class is a bracket expression, which will be covered later. In our example, `[a-f0-9]` signifies that we are looking for letters a through f and numbers 0 through 9.

### Bracket Expressions
/^#?`([a-f0-9]{6}|[a-f0-9]{3})`$/
Brackets are used to signify specific characters we want to match. Bracket expressions are used to identify these patterns, and are also known as positive character groups because it outline's the expression's inclusivity. In our example, our expression is two character classes held together with an or operator.

### Greedy and Lazy Match
/^#`?`([a-f0-9]{6}|[a-f0-9]{3})$/
Greedy and Lazy matches signify the parameters of the match search. A greedy match will try to match as many times as possible, while a lazy match will try to match the least amount of times possible. In our example, `?` is a lazy expression because it's trying to match as few occurances as possible.

## Author

Made by: Bernie Migo\
Github: https://github.com/bmigo/regex