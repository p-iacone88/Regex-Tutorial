# Regex Tutorial

In this guide I'd like to walk through some of the details of Regex, otherwise known as regular expression syntax. We'll start by breaking down each component of this URL matching regex by providing a segment of the code example followed by a detailed explanation. As a web development student, understanding regex can be extremely helpful for dissecting and understanding search patterns defined in code.

## Summary

Let's look at this regex `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/` which is used to match or validate a URL. This line dissects the components such as domain, protocol, path, and optional parameters.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

```javascript
/^
```

```javascript
/$
```

To start, this regular expression uses two anchors; one to mark the beginning of the string and the other to mark the end of the string. The `^` anchor denotes the start of the string, while the `$` anchor asserts the end. This beginning and end combination will ensure the entirety of the string will be matched and everything in between is to be checked.

### Quantifiers

```javascript
([\/\w \.-]*)*
```

Quantifiers are the symbols to define the number of occurrences of the preceding character or group. The `*` quantifier is used to signify zero or more, so the proceeding elements are allowed to not be present at all, or they can appear as many times as used in the string being tested.

In this case, forward slashes`/`, word characters `\w`, spaces, dots `.`, and hyphens `-` can be used. The `* ` means that the URL path can occur many times or not at all due to the variety of URL structures.

### Grouping Constructs

```javascript
(https?:\/\/)?
```

The use of parentheses for grouping constructs in regex enables the accurate application of quantifiers to specific regex elements. In this example, the parentheses are used to group the protocol section, as shown in the JavaScript code snippet.

Inside of the group, `https?` represents the protocol section. `s?` means that the 's' is optional so that either secure (https) or non-secure (http) protocols can be accepted.

The `:\/\/` incorporates escape characters to make sure the regex separates the protocol from the rest of the URL.

The last `?` signifies the protocol section is optional, so that a URL without a specified protocol can be accepted.

### Bracket Expressions

```javascript
[a-z\.]
```

The character class is defined here as needing to match lowercase letters, [a-z]. `\.` means that it must match a literal dot. So the characters must be lowercase letters and dots.
This is used to validate the top-level domain of a URL, ie., '.com.'
`{2,6}` following the character class specifies that the top-level domain needs to consist of at least 2 and no more than 6 characters to align with the common patterns.

### Character Classes

```javascript
([\da-z\.-]+)
```

The role of character classes is to make distinctions between various types of characters, such as separating letters from digits.
`\d` will match any digit [0-9]. `a-z` will match any lowercase letter, `\.` will match a dot, and `-` will match a hyphen.
This segment of the regex looks for a sequence that can contain digits, lowercase letters, periods (dots), or hyphens. This is searching the domain name portion of the URL.

### Character Escapes

```javascript
\/
```

Inside of this URL-matching regex, the escape sequence is used to match literal character. In this case it must strictly match the forward slash character provided after the escape character. Using any character after an escape means that it must be precisely matched and there are to be no other special regex interpretations.
In a URL, the forward slash is an essential component, so in this regex the accurate matching is necessary.

## Author

Philip Iacone is an aspiring full stack web developer located in Philadelpha, PA.
https://github.com/p-iacone88
