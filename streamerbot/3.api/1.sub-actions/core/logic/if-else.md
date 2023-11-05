---
title: If/Else
description: Logic Sub-Actions Reference
published: true
date: 2023-04-08T00:27:06.138Z
tags: logic, if, else
editor: markdown
dateCreated: 2022-01-09T11:33:31.443Z
---

## Overview
The If sub-action performs a logical test on the contents of an `Argument` and if the result is true it will perform a named action and then either break the action or let it continue

> If the test comes back `False` the rest of the IF statement will be ignored and the action will always continue to the next sub-action 
{.is-warning}

![logic-if.png](/logic-if.png =400x)

## Configuration
### Variable
This is the `Argument` name to test

> If you are still using v0.14 or belowm do not use % symbols in the variable name, for v0.15 and up it % symbols will be ignored in the Variable name
{.is-info}

### Operator
The Type of logical test to perform. Valid options are `Equals`, `Not Equals`, `Contains`, `Regex Match`, `Less Than`, `Greater Than` & `Does Not Exist`

### Value
The value for comparison 

### Do Action
The `Action` to perform if the logic test is true

If the `Run Action Immediately` checkbox is ticked, this will run the action outside of its normal queue as if it were a subroutine of the current action, Streamerbot will return to this point in the action after it has completed

If the box is unchecked then Streamerbot will queue it as normal as a completely separate action and then move on immediately to the next sub-action

### Then
This specifies if the Action should `Continue` or `Break` after performing its named Action. This flag will only trigger if the test was `True`, if not it will always `Continue`


## RegEx Match
The RexEx operator is used to perform a regular expression match on the contents of an `Argument` defined in `Value`.

### Defining a RegEx
Using tools like [RegExr](https://regexr.com) you can more easily see a breakdown of the RegEx syntax and how it will work to make sure that it functions how you intend it. You can also see the [C# RegEx Docs](https://learn.microsoft.com/en-us/dotnet/api/system.text.regularexpressions.regex?view=netframework-4.7.2) for C# specific syntax but you can also use JavaScript based RegEx syntax and most RegEx Engines support it.

---

- [<i class="mdi mdi-chevron-left"></i> **Logic Sub-Actions *Go Back***](/Sub-Actions/Logic)
{.btn-grid .my-5}