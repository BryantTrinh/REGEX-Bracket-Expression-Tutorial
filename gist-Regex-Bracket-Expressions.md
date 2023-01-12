# Title (replace with your title)

Before we get into Bracket Expressions, we must talk about what Regex is. Regex is a shorthand term for "regular expressions". These are patterns that can be used to match characters in a string.

In Javascript, we see Regex regularly in objects.

Some common cases of Regex are in strings, where we use:
-test()
-match()
-replace()
-replaceAll()
-search()
-split()

## Summary

Bracket Expressions ' [] '.
  - These brackets hold meaning, where when we use them, it indicates a set of characters to match.


## Table of Contents

- [Bracket Expressions](#bracket-expressions)

### Bracket Expressions

Some bracket expressions examples are as follows:

  - Just using brackets:
    - 'github'.match(/[ghijklmnop]/)
     - matches found are: 'g', 'h', 'i'

  - Here we can also use this '^' character, which will not find what is inside the bracket.
   -'github'.match(/[^ghijklmnop]/)
      - matches found are: 'b', 't', u'.

  - Another use, is the 'i' flag. This 'i' flag will ignore capitalization/ case sensitive strings.
    - 'github'.match(/[GHIJKLMNOP]/i)
      - matches found are: 'g', 'h', 'i'
    - If we do not use the 'i' flag, here is what it would look like:
     -'github'.match(/[GHIJKLMNOP]/)
      - No matches are found.

Next, we have curly braces, where they are used to specify an exact amount of matches. We use these after an expression, where it will only match something a {X} amount of times.

  -Lets say we want to do an expression that is \oo{1}\
    - 'exploration'.match(/na{1}/)
      - No matches are found.
    - 'book'.match(/oo{1}/)
      - Matches found are 'oo', in 'book'.
    - 'alfalfa'.match(/alf{2}/)
      - Matches found are 'alfalf'.

  Additionally, we canalso include a comma to specify more than one amount. {2,3}, which means between 2 and three times.
  - 'apple'.match(/a{2,3}/)
    - No match found
  - 'applee'.match(/a{2,3}/)
    - Matches found are "ee"
  - 'appleee'.match(/a{2,3}/)
    - Matches found are "eee"

Finally, we have parantheses, which represent remembered matches. This is used to find and replace operations or if you want to find part of a match. When a match is found or remembered, you can use $n to refer to it. You can use $1 - $9 or $& to refer to the entire match.

  - 'Firstname Lastname'.match(/([A-Za-z]+)\s([A-Za-z]+)/) 
    - Matches 'First Lastname' with 'First', and is remembered as $1 and 'Lastname' as $2.
  - 'Firstname Lastname'.replace(/([A-Za-z)+)\s([A-Za-z]+)/, '$1')
    - returns 'Firstname'
  - 'Firstname Lastname'.replace(/(A-Za-z)+)\s(A-Za-z)+)/, '$2, $1')
    - returns 'Lastname, Firstname'
  - 'John Doe'.replace(/([A-Za-z])+\s([A-Za-z]+)/, '$&')
    - returns 'John Doe'

## Author

Bryant Trinh, current web developer student.

https://github.com/BryantTrinh/

