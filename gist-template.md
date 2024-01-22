# Regex Tutorial

In this guide I'd like to walk through the details of Regex, otherwise known as regular expression syntax. We'll start by breaking down each component by providing a code example and a detailed explanation. As a web development student, understanding regex can be extremely helpful for dissecting and understanding search patterns defined in code.

## Summary

Let's look at this regex `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/` which is used to match or validate a URL. This line dissects the components such as domain, protocol, path, and optional parameters.

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

```javascript
/^
```

To start, this regular expression uses the `^` anchor to denote the start of the string, while the `$` anchor asserts the end. This beginning and end combination will ensure the entirety of the string will be matched.

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
