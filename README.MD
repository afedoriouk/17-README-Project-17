# REGEX and its' use in codin and web develoment
Regular Expressions - REGEX

Regular Expressions is a platfom for matching and verificatrion of data which is presented in the form or sequence of several characters that specify a search pattern in the text.
These patterns could be used by string searching algorithms. Regular expressions use couple of methods. One is for input validation and second is for (find and replace).
Regular Expressions is widely used to validate phone numbers email addresses website addreses...etc

## Below are few example of the Regular Expressions in use:

\d -> any 'meta' charachter (number)
\d\d\d-\d\d\d-\d\d\d\d -> phone number
(?)\d{3}[-.)]\d{3}[-.] \d{4}

.* button (DOT STAR)
. Dot= any charachter
* Star= "wild card"
[a-z]=any character a through z
[^a-z] {3}= any three numbers 
^=anything but the selected characters
[A-Z] look for only capital letters
\b[A-Za-z]{4}\b this expression means that this is matching four letter words with ONLY capital or lower case letters
\w = inludes letters and numbers
match email addresses:
[\w]+@\w+\.(net|com|edu)
"alternation" \. = (.) actual dot
charachter class

Regular Expressions USED FOR FORM VALIDATION
If the address is missing "@" symbol or Upper or lower case of the letters...etc Regular Expressions Validation will return false.

Capturing Roots
validating speliing characters
l[yi]nk = any characters with "lynk" and "link"

## Summary

The method "str.match(regexp)" looks for matches: all of them if there’s g flag, otherwise, only the first one.
The method "str.replace(regexp, replacement)" replaces matches found using regexp with replacement: all of them if there’s g flag, otherwise only the first one.
The method "regexp.test(str)" returns true if there’s at least one match, otherwise, it returns false.
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
### Quantifiers
### OR Operator
### Character Classes
### Flags
Regular expressions may have flags that affect the search.
A regular expression consists of a pattern and optional flags: g, i, m, u, s, y.
Without flags and special symbols, the search by a regexp is the same as a substring search.
"i" With this flag the search is case-insensitive: no difference between A and a
"g" With this flag the search looks for all matches, without it – only the first match is returned.
"m" Multiline mode
"s" Enables “dotall” mode, that allows a dot . to match newline character \n
"u"Enables full Unicode support. The flag enables correct processing of surrogate pairs. 
"y" “Sticky” mode: searching at the exact position in the text

### Grouping and Capturing
### Bracket Expressions
Bracket Expression: []
Code Snipet: [a-l0-9]
Description: Bracket expression is a method in regex that is going to match specific characters or paterns. For example: (alphabetic, numeric, special, symbols). All of the characters are defined with the brackets around the characters that presented for the match.

### Greedy and Lazy Match
### Boundaries
### Back-references
### Look-ahead and Look-behind
## Author

https://github.com/afedoriouk

AS A web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines

GIVEN a regex tutorial
WHEN I open the tutorial
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile
WHEN I click on the links in the table of contents
THEN I am taken to the corresponding sections of the tutorial
WHEN I read through each section of the tutorial
THEN I find a detailed explanation of what a specific component of the regex does
WHEN I reach the end of the tutorial
THEN I find a section about the author and a link to the author’s GitHub profile


## EXAMPLES
Matching a Hex Value – /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Matching a URL – /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
Matching an HTML Tag – /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/