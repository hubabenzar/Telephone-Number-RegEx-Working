# Telephone-Number-RegEx-Working
This Regular Expression (RegEX) is my solution to a telephone number that is flexible to be used by most people.

It allows for the use of extensions or ext at any point in the code.
The only requirment is for the input/string to contain three characters with the option of having spaces in between, but not symbols or alpha numericals.

Feel free to let me know if this code can be improved.

## Code:
```
^[\W\d]*(?:\s*\d\s*){3,}(?:\W*ext(ension)*\W*\d*)*$
```
## Test it out:
Regexr.com/5753o


## Explanation:
```
^             = Beginning. Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled.
[             = Character set. Match any character in the set.
  \W          = Not word. Matches any character that is not a word character (alphanumeric & underscore).
  \d          = Digit. Matches any digit character (0-9).
]             = End of character set.
*             = Quantifier. Match 0 or more of the preceding token.

(?:           = Non-capturing group. Groups multiple tokens together without creating a capture group.
  \s          = Whitespace. Matches any whitespace character (spaces, tabs, line breaks).
  *           = Quantifier. Match 0 or more of the preceding token.
  \d          = Digit. Matches any digit character (0-9).
  \s          = Whitespace. Matches any whitespace character (spaces, tabs, line breaks).
  *           = Quantifier. Match 0 or more of the preceding token.
)             = End of Non-capturing group.
{3,}          = Quantifier. Match 3 or more of the preceding token.

(?:           = Non-capturing group. Groups multiple tokens together without creating a capture group.
  \W          = Not word. Matches any character that is not a word character (alphanumeric & underscore).
  *           = Quantifier. Match 0 or more of the preceding token.
  ext         = Word to match. ext at least.
  (ension)    = Word extension. This is an extension to the word
  *           = Quantifier. Match 0 or more of the preceding token.
  \W          = Not word. Matches any character that is not a word character (alphanumeric & underscore).
  *           = Quantifier. Match 0 or more of the preceding token.
  \d          = Digit. Matches any digit character (0-9).
  *           = Quantifier. Match 0 or more of the preceding token.
)             = End of Non-capturing group.
*             = Quantifier. Match 0 or more of the preceding token.
$             = End. Matches the end of the string, or the end of a line if the multiline flag (
```
