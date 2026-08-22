---
title: If / Else
description: Perform conditional logic based on variable contents
parameters:
  - name: Input
    type: Text
    required: true
    description: |
      The value to be tested. Performs full parsing of `%arguments%`{lang=cs}, `~persistedGlobals~`{lang=cs} and `$inlineFunctions()$`{lang=cs}
      ::warning
      Unlike earlier version of Streamer.bot, arguments **must** be enclosed in `%...%` in order for their values to be tested<br/>
      If using `Does Not Exist`, you **must** use *only* the argument name without the `%`.
      ::
  - name: Operator
    type: Select
    required: true
    default: Equals
    description: |
      Choose the type of test to perform on the selected variable

      - `Equals`: Check if the variable equals a given value
      - `Not Equals`: Check if the variable does not equal a given value
      - `Contains`: Check if the variable contains the given value
      - `Regex Match`: Use a Regular Expression to match variable contents
      - `Less Than`: Check if a numeric variable is less than a given value (does NOT include the set value)
      - `Greater Than`: Check if a numeric variable is greater than a given value (does NOT include the set value)
      - `Does Not Exist`: Check if the variable name is defined at all
      - `Equals (Ignore Case)`: Check if a string variable equals a given value, case insensitive
      - `Not Equals (Ignore Case)`: Check if a string variable does not equal a given value, case insensitive
      - `Is Null or Empty`: Check if a variable is `Null`{lang=cs} or empty

      ::tip
        **Regular Expressions (RegEx) are extremely powerful!**<br>
        :icon{name=i-mdi-chevron-right} You can use tools like [regex101](https://regex101.com) and [RegExr](https://regexr.com) to view and test your expressions.
      ::
  - name: Auto Type
    type: Toggle
    default: true
    description: |
      Without Auto Type, values are treated as text, or `string`{lang=cs} variables, which may result in surprising results like "`15`" being `Less Than` "`2`"

      Enable `Auto Type` to automatically determine the type for the variable value. This is usually what you want, unless you are deliberately performing lexicographic (alphabetical) comparison on text which might happen to contain numbers.

      For example:
      - `0`{lang=cs} can be auto-typed to a numeric type such as `int`{lang=cs} or `long`{lang=cs}
      - `true`{lang=cs} or `false`{lang=cs} can be auto-typed to a `bool`{lang=cs}
  - name: Value
    type: Text
    required: true
    description: |
      Enter the value you would like to use for comparison.

      This field is parsed, so may contain other `%arguments%`{lang=cs}, `~persistedGlobals~`{lang=cs} and `$inlineFunctions()$`

variables:
  - name: match.count
    type: int
    description: |
      Only when using "Regex Match" as the operator.

      The number of match groups (named or unnamed) in the regex.

      Note that this is always 1 more than the number of parentheses groups, as the entire match is implicitly group 0.
    value: 3
  - name: match[<index>]
    type: string
    description: |
      Only when using "Regex Match" as the operator.

      The text matching each indexed capture group.

      Index 0 is the entire matching text, and the first parenthesized group is 1.
    value: 'matching word'
  - name: <groupName>
    type: string
    description: |
      Only when using "Regex Match" as the operator.

      When using named capture groups (e.g, `(?'points'\d+)` or `(?<points>\d+)` ), each named capture group becomes an argument containing the text of the match.
    value: '123'
---

::collapsible{name="If/Else Flow Diagram by pwnyy"}
  ![If-Else Flow Chart by pwnyy (Right-Click to open full size in a new tab)](/assets/1.get-started/assets/if-else-flowchart.png)
::