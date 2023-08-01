# Reular Expressions

Some of the scariest looking code can be regular expressoins or RegEx. They can seem long and cryptic-like. But I'm here to break down exactly how these snippets of code work so you can use them in your own code to quickly match an email.

## Summary of Matching an Email

Let's jump into it. This is a regular expression. It is basically a pattern that gets read to match items.
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
This code matches an email.

## Table of Contents

-   [Regex Components](#regex-components)
-   [Anchors](#anchors)
-   [Quantifiers](#quantifiers)
-   [OR Operator](#or-operator)
-   [Character Classes](#character-classes)
-   [Flags](#flags)
-   [Grouping and Capturing](#grouping-and-capturing)
-   [Bracket Expressions](#bracket-expressions)
-   [Greedy and Lazy Match](#greedy-and-lazy-match)
-   [Boundaries](#boundaries)
-   [Back-references](#back-references)
-   [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

There are two ways you can go about writting a regular expression. The first way is using a regex constructor. This uses a string or constructor as it's first param. The other is a literal notation. Literal notations start and end with a slash. When looking at the regular expression for matching an email you can see that it starts and ends with a slash. This means we are using literal notation.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

My name is Larissa Stack. I go by Rissa. I am currently a student at University of Arizona to become a full-stack web developer. If you have any questions, please reach out to me on GitHub. https://github.com/RissaStack
