# Regular Expressions 

## Summary
Regular expression otherwise known as regex, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Table of Contents-Regex Components

- [Anchors](###anchors)
- [Quantifiers](###quantifiers)
- [OR Operator](###or-operator)
- [Character Classes](###character-classes)
- [Grouping and Capturing](###grouping-and-capturing)
- [Bracket Expressions](###bracket-expressions)
- [Greedy and Lazy Match](###greedy-and-lazy-match)
- [Back-references](###back-references)
- [Look-ahead and Look-behind](###look-ahead-and-look-behind)

## Regex Components

### Anchors
- Anchors are a type of regex components that start and ends a srting. 
- To demontrate how the anchor component would work in case of a matching an an email:
 `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
- The anchor ** ^ ** and ** $ ** demonstrates that the code must start with `^([a-z0-9_\.-]+)` 
and end with `.([a-z\.]{2,6})$`.To pass the match test the given the anchor component must start and end with the above mentioned paremeters without any errors. 

### Quantifiers
- A quantifier component is used to determine how many times a perticular character or group of characters reccurs or needs to be present to pass the match test.
- certain charecters that are repeated often are as follows:
 -- `*` Matches 0+ occurrences of the section that precedes it.
 -- `+` Matches more than 1 occurrences of the section it follows.
 -- `?` Matches 0 / 1 occurrences of the section it follows.
 - For instance in the case of the match  an email:
 -- The quantifier component will result in `([a-z0-9_\.-]+)`. This will ensure a match for any string that contains a-z, 0-9, _, ., or -. The quantifier ** + ** states that the element must contain at least one of this criteria in order to qalify for a match. 
 
### OR Operator
- The OR operator also denoted as | operator ( `|` referes to the logical Or) 
- Can be used to match chatercters or expressions of either the left or the right side of the ** or operator **
- In the instance of match an email `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`- the OR operator is not present. 
- A possible example of or operator could be found in the matching a HTML Tag - `/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/`- wherein the left side `/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>` is sperated with the `|` from the right side  `\s+\/>)$/`.

### Character Classes
- A character class refers to a set of characters enclosed within square brackets `[]`.
- Specifies the characters that will successfully match a single character from a provided input string. 
- Syntax for the same would be:,
- ** \d ** - matches a single character that is a ** digit ** between 0 to 9
- ** \w ** - matches a ** word ** character [A-Za-z0-9_]
- ** \s ** - matches a ** whitespace ** character
- ** \D ** - matches a ** NON-digit ** character
In the case of macthing an email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
-- `\d` would represents a single digit ranging from the numerical values 0 to 9 after the `@` sign in email address. this string will only match a single digit such as "2", but not "22" or "12".

### Grouping and Capturing
- Capturing groups is a method used to group or enclose multiple characters in one unit. 
- These groups are created by placing the characters to be grouped inside a set of parentheses
  ().
- In the instance of matching an email address: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
-- `([a-z0-9_\.-]+)`- first group in our regex code that would match the email name for example swapna.
-- `([\da-z\.-]+)`- second group in our regex code that would match the email service for example gmail. 
-- `([a-z\.]{2,6})`- third group in our regex code that would match the domain such as .com.
  
### Bracket Expressions

### Greedy and Lazy Match

### Back-references

### Look-ahead and Look-behind
