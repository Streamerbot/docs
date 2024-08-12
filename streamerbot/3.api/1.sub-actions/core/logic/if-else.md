---
title: If / Else
description: Perform conditional logic based on variable contents
parameters:
  - name: Variable
    type: Text
    required: true
    description: |
      Enter the variable / argument name to test
      ::warning
      If the variable does not exist, the entire sub-action will be skipped unless you are using the `Is Null or Empty` operator.
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
      - `Less Than`: Check if a numeric variable is less than a given value
      - `Greater Than`: Check if a numeric variable is greater than a given value
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
    default: false
    description: |
      By default, values which have not already been typed are treated as text, or `string`{lang=cs} variables.

      Enable `Auto Type` to automatically determine the type for the variable value.

      For example:
      - `0`{lang=cs} can be auto-typed to a numeric type such as `int`{lang=cs} or `long`{lang=cs}
      - `true`{lang=cs} or `false`{lang=cs} can be auto-typed to a `bool`{lang=cs}
  - name: Value
    type: Text
    required: true
    description: |
      Enter the value you would like to use for comparison.

      This can contain other `%variables%`{lang=cs}

      ::warning
      You cannot use `~globalVariables~`{lang=cs} directly. Use the [Global Get](/api/sub-actions/core/global/global-get) sub-action to first load it into a local argument.
      ::
  - name: Do Action
    type: Select
    default: None
    description: Select an action to execute if the comparison is `true`{lang=cs}
  - name: Run Action Immediately
    type: Toggle
    default: true
    description: |
      By default, the selected action will be executed outside of its normal queue and treated as a subroutine of the current action, waiting for completion before moving on to the next sub-action.

      Disable this option to queue the action as normal and immediately move on to the next sub-action
  - name: Then
    type: Select
    default: Continue
    description: |
      Choose whether or not the current action should continue if the comparison was `true`{lang=cs}

      - `Continue`: Continue execution as normal, moving on to any subsequent sub-actions
      - `Break`: Stop the current action, any subsequent sub-actions will not be executed.
  - name: Else Condition -> Do Action
    type: Select
    default: None
    description: Select an action to execute if the comparison is `false`{lang=cs}
  - name: Else Condition -> Run Action Immediately
    type: Toggle
    default: true
    description: |
      By default, the selected action will be executed outside of its normal queue and treated as a subroutine of the current action, waiting for completion before moving on to the next sub-action.

      Disable this option to queue the action as normal and immediately move on to the next sub-action
  - name: Else Condition -> Then
    type: Select
    default: Continue
    description: |
      Choose whether or not the current action should continue if the comparison was `false`{lang=cs}

      - `Continue`: Continue execution as normal, moving on to any subsequent sub-actions
      - `Break`: Stop the current action, any subsequent sub-actions will not be executed.
---

::disclosure
If/Else Flow Diagram by pwnyy

#content
  ::small{.text-gray-400}
  Right-Click -> Open in New Tab to view full size
  ::
  ![If-Else flowchart](/1.get-started/assets/if-else-flowchart.png)
::