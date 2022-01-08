# Computer Science for JavaScript- Regex Tutorial

Welcome web development students, this page will serve as a tutorial explaining all the different search patterns that a specific regex defines.

## Summary

Regular expressions or regex are useful in extracting information from text by searching for matches of a specific pattern based on a specific sequence of ASCII or unicode characters.

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

Anchors

- `^ `- The caret anchor matches the beginning of a string or line.

- `$ `- The dollar sign anchor matches the end of a String or line.

### Quantifiers

Quantifiers

- `*`- Matches the previous element 0 or more times.
- `+`- Matches the previous element 1 or more times.
- `?`- Matches the previous element 0 0r 1 time. -`{n}`Matches the previious element exactly n times.
- `{n,}`- Matches the previous element n or more times.
- `{n,m}`- Matches the previous element between n and m times.

### OR Operator

OR

The OR operator In a regular expression it is expressed with a vertical character and allows you to compose regular expression patterns to match any one out of a set of alternative choices.

### Character Classes

Character Classes

- `\w `- matches any character that is a letter(capital-lower case), number, or underscore.
- `\W`- - matches any character that is Not a letter(regardless of case) number, or underscore
- `\d `- matches any character that is a number.
- `\D `- matches any character that is Not a digit
- `\s `- matches any character that is a whitespace character such as- tabs,returns,spaces and form feeds
- `\S `- matches any character that is Not a whitespace character.

### Flags

Flags

- `i- Ignore Casing `- Makes the expression search case-insensitively.
- `g- Global`- Makes the expression search for all occurences.
- `s- Dot All`- Makes the wild character . match newlines as well.
- `m- Multiline`- Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning an ending of the whole string.
- `y- Sticky`- Makes the expression start its searching from the index indicated in its lastIndex property.
- `u- Unicode`- Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.

### Grouping and Capturing

Grouping and Capturing

Grouping and Capturing are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses. For example, the regular expression (cat) creates a single group containing the letters "c" "a" and "t"

### Bracket Expressions

Bracket Expressions

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set.A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions- ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.

### Greedy and Lazy Match

- `Greedy`- means match longest possible string.

- `Lazy`- means match shortest possible string.

### Boundaries

Boundaries

The `\b`- is an anchor like the caret and the dollar sign. It matches at a position that is called a “word boundary”. This match is zero-length.

`\B`- is the negated version of `\b`. `\B`- matches at every position where `\b`- does not. Effectively, `\B`- matches at any position between two word characters as well as at any position between two non-word characters.

Since digits are considered to be word characters, `\b4\b`- can be used to match a 4 that is not part of a larger number. So saying `\b`- matches before and after an alphanumeric sequence is more exact than saying “before and after a word”.

### Back-references

Back-references

Backreferences match the same text as previously matched by a capturing group. let's believe you want to match a pair of opening and closing HTML tags, and the text in between. By leveraging the opening tag into a backreference, we can reuse the name of the tag for the closing tag.

> For Example- <([A-Z][0-9]_)\b[^>]_>.\_?</\1>

This regex contains only one pair of parentheses, which capture the string matched by [A-Z][0-9]\_.

This is the opening HTML tag. The backreference \1 references the first capturing group. \1 matches the exact same text that was matched by the first capturing group. The / before it is a literal character. It is simply the forward slash in the closing HTML tag that we are trying to match.

### Look-ahead and Look-behind

Look-ahead and Look-behind

- `(?=ABC)`- is a postive lookahead and it matches a group after the main expression without including it in the result.
- `(?!ABC)`- is a negitive lookahead and it specifies a group that can not match after the main expression (if it matches, the result is discarded)
- `(?<=ABC>)`- is a postive lookbehind and matches a group before the main expression without including it in the result.
- `(?<!ABC)`- is a negitive lookbehind and Specifies a group that can not match before the main expression (if it matches, the result is discarded).

## Author

This tutorial was brough tot you by Steven Dorvil, a web development student studying both front end and backend development. This tutorial served as both a studying refreshment and teaching moment, to be able to take a topic as complex as this one and break it down into simple components. I hope you enjoyed this tutorial, and please provide feedback.

[Steven Dorvil](https-//www.github.com/dorvilsteven)

[Email](dorvilsteven@gmail.com)
