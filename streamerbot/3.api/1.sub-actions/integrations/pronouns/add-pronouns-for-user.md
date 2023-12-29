---
version: 0.2.2
---

# Add Pronouns for User
Get the pronouns from a user.
:image-preview

## Parameters
### `User Login`
The user's login name.

### `Variable Prefix`
The name before the variable to differentiate between multiple of these Sub-Actions.

For example when the variable prefix is `user-one`, variable would consist of: `user-one.pronounPronoun`, `user-one.pronounReflexive`, etc.

## Variables
:variables-description

::callout{icon="i-mdi-lightbulb" color=primary}
Change the `variable-prefix` in this code to the variable prefix you've filled in earlier.
::

Name | Description
----:|:------------
`variable-prefix.pronounPronoun` | The user's pronoun
`variable-prefix.pronounReflexive` | The reflexive pronoun
`variable-prefix.pronounPastTense` | The pronoun in the past tense
`variable-prefix.pronounSubjectLower` | The pronoun subject in lowercase
`variable-prefix.pronounObjectLower` | The pronoun object in lowercase
`variable-prefix.pronounPossessiveLower` | The possessive pronoun in lowercase 
`variable-prefix.pronounPronounLower` | The user's pronoun in lowercase
`variable-prefix.pronounReflexiveLower` | The reflexive pronoun in lowercase
`variable-prefix.pronounPastTenseLower` | The past tense pronoun in lowercase
`variable-prefix.pronounCurrentTense` | The pronoun in the current tense
`variable-prefix.pronounCurrentTenseLower` | The lowercase pronoun in the current tense
`variable-prefix.pronounPluralLower` | The pronoun plural in lowercase
`variable-prefix.pronounPossessive` | The possessive pronoun
`variable-prefix.pronounObject` | The pronoun object e.g. `Him`
`variable-prefix.pronounSubject` | The pronoun subject e.g. `He`
`variable-prefix.pronouns` | The full pronouns from the user e.g. `(He/Him)`
`variable-prefix.pronounLastCached` | The date and time when the pronouns where last cached

## C# Usage
:csharp-method