# Palindrome Checker Algorithm

This repository contains the pseudocode for a simple algorithm that checks whether a given word is a palindrome. A palindrome is a word that reads the same backward as forward, such as 'radar' or 'level'.

## Algorithm Description

The algorithm uses a recursive function `checkIF` that compares characters from both ends of a string, progressively moving towards the center. It determines if the input string is a palindrome and returns a boolean value - `TRUE` if it is a palindrome, or `FALSE` otherwise.

### Function: `checkIF`

- **Parameters**: 
  - `text`: STRING - The word to check.
  - `startIndex`: INTEGER - The starting index for comparison.
  - `endIndex`: INTEGER - The ending index for comparison.
- **Returns**: BOOLEAN - `TRUE` if the word is a palindrome, `FALSE` if not.

```pseudocode
FUNCTION checkIF(text: STRING, startIndex, endIndex: INTEGER) : BOOLEAN
BEGIN
    IF (startIndex >= endIndex) THEN
        RETURN TRUE;
    ELSE_IF (text[startIndex] = text[endIndex]) THEN
        RETURN checkIF(text, startIndex + 1, endIndex - 1);
    ELSE
        RETURN FALSE;
    END_IF
END
