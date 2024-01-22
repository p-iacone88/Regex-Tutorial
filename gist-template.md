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

```javascript
([\/\w \.-]*)*
```

Quantifiers are the symbols to define the number of occurrences of the preceding character or group. The `*` quantifier is used to signify zero or more, so the proceeding element is allowed to not be present at all, or it can appear as many times as used in what is being tested.

### Grouping Constructs

```javascript
(https?:\/\/)?
```

The use of parentheses for grouping constructs in regex enables the accurate application of quantifiers to specific regex elements. In this example, the parentheses are used to group the protocol section, as shown in the JavaScript code snippet.

### Bracket Expressions

```javascript
[a-z\.]
```

The character class is defined here as needing to match lowercase letters, [a-z]. `\.` means that it must match a literal dot. So the characters must be lowercase letters and dots.

### Character Classes

```javascript
([\da-z\.-]+)
```

The role of character classes is to make distinctions between various types of characters, such as separating letters from digits.
`\d` will match any digit [0-9]. `a-z` will match any lowercase letter, `\.` will match a dot, and `-` will match a hyphen.
This segment of the regex looks for a sequence that can contain digits, lowercase letters, periods (dots), or hyphens. This is searching the domain name portion of the URL.

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
