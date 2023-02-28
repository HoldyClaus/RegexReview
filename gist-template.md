#Holden's Regex Expression

A **regex**, which is short for **regular expression**, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. 

## Summary

In this assignment I will be going over the Regular Expression of Email:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

Emails are made up of characters and numbers with an @ symbol, then folled up with more characters and numbers then a period then repeat of more characters. Moving forward to the regex comparison of the email. /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors

Anchor operators are special characters used in regular expressions (regex) to match specific positions in a string. There are two types of anchor operators:

^ (caret) - This anchor operator is used to match the beginning of a string. For example, the regex "^Hello" will match any string that starts with "Hello", such as "Hello world" or "Hello there".

$ (dollar sign) - This anchor operator is used to match the end of a string. For example, the regex "world$" will match any string that ends with "world", such as "Hello world" or "Goodbye world".

It's important to note that these anchor operators only match the position in the string, not the actual characters themselves. This means that if you want to match a string that starts with "Hello" and ends with "world", you would use the regex "^Hello.world$". The "." in the middle matches any character zero or more times, so it will match any characters between "Hello" and "world".

### Quantifiers

Quantifier operators are special characters used in regular expressions (regex) to specify the number of times a pattern should match in a string. They allow you to match multiple occurrences of a pattern without having to write out the pattern multiple times. Here are the most common quantifier operators:

(asterisk) - Matches zero or more occurrences of the preceding pattern. For example, the regex "ab*c" will match "ac", "abc", "abbc", "abbbc", and so on.
(plus sign) - Matches one or more occurrences of the preceding pattern. For example, the regex "ab+c" will match "abc", "abbc", "abbbc", and so on, but not "ac".
? (question mark) - Matches zero or one occurrence of the preceding pattern. For example, the regex "ab?c" will match "ac" or "abc", but not "abbc".

{n} - Matches exactly n occurrences of the preceding pattern. For example, the regex "a{3}" will match "aaa".

{n,} - Matches n or more occurrences of the preceding pattern. For example, the regex "a{3,}" will match "aaa", "aaaa", "aaaaa", and so on.

{n,m} - Matches between n and m occurrences of the preceding pattern. For example, the regex "a{2,4}" will match "aa", "aaa", or "aaaa", but not "a" or "aaaaa".

### OR Operator

The "or" operator in regular expressions (regex) is represented by the vertical bar character, "|". It allows you to match one of several alternative patterns. For example, the regex "cat|dog" will match either "cat" or "dog".

### Character Classes

In regular expressions (regex), a character class is a set of characters that can be matched as a single character in a string. They are enclosed in square brackets [ ], and any character inside the brackets will match any character in the set.

[\d] - Matches any digit character.

### Flags

In regular expressions (regex), flags are optional parameters that modify how a pattern is matched. They are represented by single-letter codes that are appended to the end of a regex pattern, following the closing delimiter.

### Grouping and Capturing

In regular expressions (regex), grouping and capturing are used to capture and manipulate specific parts of a string. Grouping refers to the use of parentheses to group together parts of a pattern, while capturing refers to the process of capturing the substring that matches a group.

Grouping with parentheses: (cat|dog) matches either "cat" or "dog".
Capturing with parentheses: (cat|dog) captures either "cat" or "dog" as a group, which can be referred to later in the pattern or in the replacement string.
Non-capturing grouping: (?:cat|dog) matches either "cat" or "dog", but does not capture the match as a group.

### Bracket Expressions

In regular expressions (regex), bracket expressions, also known as character classes, are used to match any one of a set of characters. They are enclosed in square brackets and consist of a set of characters or character ranges.

Here are some examples of how bracket expressions can be used in regex:

[aeiou] matches any one of the characters "a", "e", "i", "o", or "u".
[0-9] matches any digit from 0 to 9.
[a-zA-Z] matches any letter, either uppercase or lowercase.
[^aeiou] matches any character that is not "a", "e", "i", "o", or "u".
You can also use shorthand codes in bracket expressions to match certain character classes, such as:

\d matches any digit (equivalent to [0-9]).
\w matches any word character (equivalent to [a-zA-Z0-9_]).
\s matches any whitespace character, such as space, tab, or newline.

### Greedy and Lazy Match

In regular expressions (regex), greedy and lazy matching refer to how the engine matches patterns in a string.

By default, regex matching is greedy, which means that the engine matches as many characters as possible while still satisfying the pattern. For example, the pattern ".*" will match any sequence of characters, including the entire string.

### Boundaries

In regular expressions (regex), boundaries are used to match specific positions in a string, rather than specific characters. Boundaries can be used to match the beginning or end of a line, word, or string.

Here are some commonly used boundary expressions:

^: Matches the beginning of a line.
$: Matches the end of a line.
\b: Matches a word boundary, which is the position between a word character (such as a letter or digit) and a non-word character (such as whitespace or punctuation).
\B: Matches a non-word boundary, which is the position between two word characters or two non-word characters.

### Back-references

In regular expressions (regex), a backreference is a reference to a previous capture group in the same pattern. Capture groups are used to group together parts of a pattern, and they can be referenced later in the pattern using a backreference.

A backreference is written as a backslash followed by a number, where the number corresponds to the position of the capture group in the pattern. For example, the first capture group is referenced using '\1', the second capture group is referenced using '\2', and so on.

### Look-ahead and Look-behind

In regular expressions (regex), lookaround is a technique used to match patterns based on the context around them, without including the context in the match. Lookaround consists of two types: look-ahead and look-behind.

Look-ahead matches a pattern only if it is followed by another pattern. It uses a positive or negative lookahead assertion, represented by '(?=pattern)' for positive lookahead and '(?!pattern)' for negative lookahead.

## Author

Holden Claus GitHub profile: https://github.com/HoldyClaus
Gist: https://gist.github.com/HoldyClaus/271e4813258bd011bea7557fbd106186