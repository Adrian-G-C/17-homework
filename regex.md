# Regex - What are they and what do they mean?

Regex is a powerful tool used for pattern matching and manipulation of text data. It provides a concise and flexible way to search, validate, and extract specific patterns from strings of characters. By constructing a regex pattern, you can define rules that describe the desired pattern you're looking for in a text. Regex finds applications in various fields, such as computer science, data analysis, text processing, and web development. Mastering regex can greatly improve your ability to efficiently work with and manipulate textual data, enabling you to solve complex problems related to patterns in a more effective manner.

## Summary

The regex expression ^(\d{3}-\d{3}-\d{4}|\(\d{3}\) \d{3}-\d{4})$ validates phone numbers in the format "###-###-####" or "(###) ###-####". It uses anchors, grouping constructs, quantifiers, the OR operator, character escapes, and character classes to ensure the phone number matches one of the specified formats.

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

The ^ and $ are considered anchors in "^(\d{3}-\d{3}-\d{4}|\(\d{3}\) \d{3}-\d{4})$." They represent the start and end of the line, ensuring that the entire line matches the specified pattern.

### Quantifiers

Quantifiers are symbols in regular expressions that specify the number of occurrences a pattern should match. In the given regex example, the quantifier used is {n}, where n represents a specific number. It indicates that the preceding pattern, in this case, \d{3}, should match exactly n occurrences.

In the regex ^(\d{3}-\d{3}-\d{4}|\(\d{3}\) \d{3}-\d{4})$, the \d{3} quantifier is used three times to match exactly three digits in both the "###-###-####" and "(###) ###-####" phone number formats, ensuring that the pattern is correctly matched.

### Grouping Constructs

Grouping constructs in regular expressions allow you to group patterns together and treat them as a single unit. They are represented by parentheses () in the regex. In the given example regex, the grouping construct is used to group two alternative patterns: \d{3}-\d{3}-\d{4} and \(\d{3}\) \d{3}-\d{4}. This ensures that the regex matches either the format "###-###-####" or "(###) ###-####" for phone numbers. The grouping construct defines the scope of the OR operator |, allowing the regex to match either pattern.

### Bracket Expressions

Bracket expressions, also known as character classes, allow you to specify a set of characters within square brackets [] that the regex engine will match. In the provided regex (\d{3}-\d{3}-\d{4}|\(\d{3}\) \d{3}-\d{4}), the bracket expression \d represents the character class for any digit (0-9). It matches any single digit within the specified range and is used to define the digits in the phone number pattern.

### Character Classes

Character classes in regular expressions are used to match a single character from a specific set of characters. They are denoted by square brackets [ ] and allow you to define a range or list of characters that the regex should match. In the example regex provided, the character class \d is used to match any digit (0-9). This allows the regex to match the numeric digits in the phone number pattern.

### The OR Operator

The "or operator" in regular expressions is denoted by the vertical bar (|). It allows you to specify multiple alternative patterns to match. In the given regex example, the | is used to create two alternative patterns separated by it. It means that the regex will match either the pattern before the | (which matches the "###-###-####" format) or the pattern after the | (which matches the "(###) ###-####" format).

### Flags

Flags in regular expressions are modifiers that change how the pattern matching is performed. They are represented by single characters or letters following the closing delimiter of the regular expression. In the regex provided above, there are no flags used. However, some common flags include "i" (case-insensitive matching), "g" (global matching), and "m" (multiline matching). Flags allow you to modify the behavior of the regular expression to suit your specific requirements.

### Character Escapes

Character escapes in regular expressions are special sequences that begin with a backslash \ and have a specific meaning. In the given regex, character escapes are used to match literal parentheses \( and \) to ensure they are interpreted as literal characters rather than having their special meaning as grouping constructs. This allows the regex to correctly match phone numbers in the format "(###) ###-####".

## Author

My name is Adrian, I am a student enrolled in Northwestern's coding bootcamp. I am passionate about technology in general and in this gist I tried to explain each part of a regex in my own words with some help from our lessons.

You can find my gihub profile in the link below.

GitHub - https://github.com/Adrian-G-C