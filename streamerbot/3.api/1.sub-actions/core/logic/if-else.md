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
---

::collapsible{name="If/Else Flow Diagram by pwnyy"}
  ::small{.text-gray-400}
  Right-Click -> Open in New Tab to view full size
  ::
  ![If-Else flowchart](/1.get-started/assets/if-else-flowchart.png)
::
