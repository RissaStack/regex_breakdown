# Regular Expressions

Some of the scariest looking code can be regular expressions or RegEx. They can seem long and cryptic-like. But I'm here to break down exactly how these snippets of code work so you can use them in your own code to quickly match an email.

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
-   [Boundaries](#boundaries)
-   [Back-references](#back-references)
-   [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

There are two ways you can go about writing a regular expression. The first way is using a regex constructor. This uses a string or constructor as its first param. The other is a literal notation. Literal notations start and end with /. When looking at the regular expression for matching an email you can see that it starts and ends with a slash. This means we are using literal notation.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors

The anchors we are using in this regex are ^ and $. The ^ means the beginning while the $ means the end.

### Quantifiers

Quantifiers are what tell your code how many characters it needs to look for to match. A few common quantifiers you may see are as followed: \* means 0 or more same characters + means 1 or more of the same characters.
? means either 0 or 1 of the same characters
{} with a number it means that exact number of the same characters.
{ , } means minimum and maximum characters with the left number being the minimum and the right being the maximum.

The quantifier we see in our regex is {2,6}. This means that there needs to be a minimum character set of 2 and a maximum character set of 6. But what characters? There is actually an easy way to tell where this requirement is added. Any time you see parenthesis they are grouping the rules to that section. In our regex, we see ([a-z\.]{2,6}) which means that our minimum and maximum characters are set to the a-z section.

### Character Classes

Character classes used to show what characters you want to include in your match. These are always shown inside brackets. Our regular expression shows character sets two different times.
The first character set is seen here [a-z0-9_\.-] .
This shows that they want to include any lowercase letter from a to z and any digit from 0 to 9. The backslash shows that we want to use the literal symbol meaning we also want to include the underscore (\_), a period (.), and a dash (-).

The second character class we see is [\da-z\.-].
The \d represents any number from 0-9. The a-z means we want to include all lowercase letters a through z. The backslash shows we want to use the literal characters for period(.) and dash(-).

The last character class we see is [a-z\.].
This includes any lowercase letter from a to z. The backslash is again showing we want to use the literal period (.).

### Flags

We do not have any flags in our regex, but they are pretty interesting to know. Flags are modifiers that can be applied to be more specific for the parameters you are looking for.

### Grouping and Capturing

Grouping is used to make a section of the expression to work as one. We discussed some of this above when we were looking at quantifiers. Parenthesis represent what parts of the code are getting grouped together.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We can see that our regex has three groups.

Group one is ([a-z0-9_\.-]+).
Group two is ([\da-z\.-]+).
Group three is ([a-z\.]{2,6}).

This grouping system allows us to easily see the code and break it into the parts of the email.

### Bracket Expressions

Bracket expressions are what show the character classes. Our bracket expressions are as followed:
[a-z0-9_\.-]
[\da-z\.-]
[a-z\.]

### Boundaries

Boundaries are used to specify special restrictions on what to match. We already looked at the boundaries we are using in our regex which were the ^ and $. As a reminder the ^ specifies the beginning of the string and the $ specifies the end of the string.

Some other important boundaries to know are \b and \B. These are word boundaries. These allow you to specify a particular word you want to look for. If you want to find the word "slip" without any other type of word like it you would put \bslip\b. If you add \Bslip\B, this will search for any word with slip in it. This would find slips and slipped.

### Matching Email Breakdown

So let's fully break down this regex using an example email.
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
example_16@gmail.com

The / at the beginning and end of the expression show we are using literal notation.
The ^ shows that this will be at the beginning of the expression.
We now have parenthesis showing we are grouping this next set of code.
The brackets show we are going into a character class. Our email may include lowercase letters a-z, digits 0-9, underscore, period, and dash. This takes care of the "example_16".
The + means there has to be at least one of those characters that we just listed.
Now we have a literal @ to match.
Then we go into another set of parenthesis that group our next set of requirements.
The brackets are showing our character class. We can have any digit 0-9, lowercase letter a-z, period, and dash. This takes care of our "gmail"
Now we have \. which represents a literal period.
Then we have another set of parenthesis to group our last set of code.
The brackets show that we are going into another character class. It can include any lowercase letter a-z and a period. We then have a quantifier saying that this character set must be at least 2 characters and at most 6 characters.

## Author

My name is Larissa Stack. I go by Rissa. I am currently a student at University of Arizona to become a full-stack web developer. If you have any questions, please reach out to me on GitHub. https://github.com/RissaStack
