# Regex Tutorial

A regex, which is short for regular expression, is a regular expression that searches for matching values/patterns within a string.

## Summary

This regex tutorial will explore the matching of a URL `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`. Each component has a specific responsibility to make sure or verify that the user enters an URL in the correct format.

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

---

Anchors asserts the current position in a string, for instance,the beginning of the string, or the end of a line.

- Beginning of String (or Line) : `^`
- End of String (or Line) : `$`

### Quantifiers

---

Quantifiers specify the number of consecutive occurrences of the character or expression directly preceding it. In our Regex example, we have three Quantifiers:

- in `([\da-z\.-]+)` the quantifier `+` applies to the expression `[\da-z\.-]` and will add the expression one or more times.

- in `([\/\w \.-]*)` the quantifier `*` applies to the expression `[\/\w \.-]` and will add the expression zero or more times.

- in `https?` the quantifier `?`
  applies to the character _s_ and will add zero or one S.

### OR Operator

---

It is used to represent a list, so it matches a string that contains one of the characters inside the list `[]`.

### Character Classes

---

Character Classes allow you to match characters inside a category.

- Matches a single _digit_ character : `\d` in `[\da-z\.-]`
- Matches a single _word_ character (letters, numbers, and underscore) : `\w` in `[\/\w \.-]`
- Matches any single character : `.` in `([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)`

### Flags

---

The Regex example inlcudes the following flag(s): `g` and `m`

- The _global_ flag is used to search for all the individual matches inside the string.
- The _multiline_ flag allows to use `^` and `$` as the beginning and end of a line, not the beginning and end of the string.

### Grouping and Capturing

---

The main way to group a section of a regex is by using `()`.

### Bracket Expressions

---

Anything inside a set of `[]` is know as a bracket expession.

### Greedy and Lazy Match

---

Greedy means your expression will match as large a group as possible, lazy means it will match the smallest group possible. In our example: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

- Greedy : `a-z`
- Lazy : `abcdefghijklmnopqrstuvwxyz`

### Boundaries

---

The metacharacter `\b` is an anchor like the `^`and `$`. It matches at a position that is called a _word boundary_.

- Word Boundary: `\b`
- Not-a-word-boundary: `\B`

### Back-references

---

Back-references are regular expression commands which refer to a previous part of the matched regular expression.Back-references are specified with backslash and a single digit. (e.g. : `\1`)

### Look-ahead and Look-behind

---

Look-ahead and look-behind, collectively called “look-around”, are zero-length assertions just like the start and end of line, and start and end of word anchors explained earlier in this tutorial.

## Author

[Esmeralda](https://github.com/)
