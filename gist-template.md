# Matching an Email REGEX Tutorial

This gist is a breakdown on how you can use a regular expression to verify that an input follows normal email parameters. The steps below will describe where each part of the expression comes from and the purpose that it serves.

## Summary

The regex I will be describing will verify a User's email address to make sure it matches the criteria of a proper email. 

Snippet: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

The anchors for this expression is the `^` at the beginning and $ at the end

### Quantifiers

This regular expression contains various Quantifiers. The second one is defined by `{2,6}` indicating that the part of the email that typically has '.com/.gov/.net/etc.' MUST have a minimum of `2` characters and a maximum of `6`.

### Character Classes

The character classes found in this expression are `\d` This is so that it knows that any digit `0-9` can be used.

### Grouping and Capturing

There are three groupings found in this expression. The first being the name of the email account: `[a-z0-9_\.-]`. The second is the website or domain name: `[\da-z\.-]`. and third is what the website/domain ends in (i.e .com, .net, .gov): `[a-z\.]{2,6}`

### Bracket Expressions

Bracket expressions represents anything that is inbetween the following: `[]`

The first is defined as follows: `[a-z0-9_\.-]` this can be broken up to say that this area can include any digit, letter, period, underscore, and/or hyphen. Second: `[\da-z\.-]` signifies that this part can contain any digit, letter, hyphen,and/or period. The third: `[a-z\.]` declares that it can end with any letter and period.

### Greedy and Lazy Match

This expression contains a `+` greedy expression that allows for the first grouping to be as long as it wants to. Another Greedy expression can be found at the end where `{}` is found, it can be anything within the range of `2-6`, it won't be the smallest possible.

## Author

This gist was written by Spencer Kyle [github](https://github.com/SpencerKyle)