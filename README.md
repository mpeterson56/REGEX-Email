# Matching an Email with REGEX –
# /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The series of characters above are not just random mumbo jumbo. That is actually REGEX code for email matching! This document will hopefully help explain the the funcionality of this code by breaking down the sections that may be easily missed

## Summary

Regular Expressions or REGEX, is used for various validation and matching of strings.
### /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 
 the above code is used for email matching within texts or to validate that what is being entered into an email section of a form is actually an email. Regex can do a whole lot but for now lets start with email matching.
## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [References](#references)
- [Author](#author)


## Regex Components

### Anchors
foreward slashes are the anchors of REGEX. code such as: /a-z/ this would allow any letter in the alphabet in lowercase format.
the carrot character:^ is used in the mail matching as a meta escape. it holds the place of where the string we want to match begins.inversly, the dollar sign:$ lets us know where this string ends.
/^exactlythis$/ would only match a string of "exactlythis"
### Quantifiers
the plus sign is used as a quatifier in this regex. this used used after a token to let us know the token can match between 1 and any amount of times. /m+/ would match m or mmm or even mmmmmmmmmm etc. we aslo use the {2,6} as a quantifier to to let us know the token prior can match between 2 to 6 times. its used in our last group for the top level doamin more commonly known as .com or .org. a word like watermalon would be long for the quatifiers to match so it will fail.


### Character Classes
the only character class we use for this email matching REGEX is: /d , this is a shortcut for writing 0-9 which allows any nemeric input.
### Flags
commonly at the end of regex, this particular code has none though.
### Grouping and Capturing
grouping happens within parenthesis () . we can see three sets of open and close parenthesis so this means we have three groups within this regex! inside the parenthesis, in the first two groups we see the plus quantifiers being used. on the third we use {2,6}. these quantifiers in the parenthesis but outside the square brackets helps quantities quantify whats in the square brackets.
### Bracket Expressions
bracket expressions are defined by open and closed square brackets. we use 3 bracket epressions in this code. these expressions are used to list the tokens we want to pass for matching. the first bracket expression:[a-z0-9_\.-] is for the username section of an email before the @ symbol. the a-z designation lets us know all letters in the alphabet are accepted, the 0-9 lets ud know all numeric character will be accepted, the underscore character lets us use the underscore character, the \. is an escaped period meaning its a normally a special character but the \ makes it a literal period, and finally the hyphen lets us match a hyphen.this expression allows 1 to any amount of characters. the second bracket expression is: [\da-z\.-] . the part part of this expression is the \d , as previously stated this is a shortcut for 0-9 whcich allows all nemeric characters, a-z again means all alphabetic characters are accepted, caped perion means a literal perion is allowed, and the hyphen lets us match a hyphen.this expression allows 1 to any amount of characters. the third bracket expression is: [a-z\.] . a-z matches any letter of the alphabet, the escaped period allows the literal period. this expression is only allowed 2 to 6 characters.



## references
https://regexr.com/


https://user-images.githubusercontent.com/100823810/179149053-4702a522-9b83-4569-afca-fb2a29b7fbc5.mp4




## Author
