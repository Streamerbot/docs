---
title: Add Pronouns for User
description: Fetch the alejo.io pronouns for a given Twitch user
version: 0.2.3
variables:
- name: pronounPronoun
  type: string
  description: The user's pronoun
  value: Theirs
- name: pronounPronounLower
  type: string
  description: The user's pronoun in lowercase
  value: theirs
- name: pronounReflexive
  type: string
  description: The reflexive pronoun
  value: Themselves
- name: pronounReflexiveLower
  type: string
  description: The reflexive pronoun in lowercase
  value: themselves
- name: pronounPastTense
  type: string
  description: The pronoun in the past tense
  value: Were
- name: pronounPastTenseLower
  type: string
  description: The past tense pronoun in lowercase
  value: were
- name: pronounCurrentTense
  type: string
  description: The pronoun in the current tense
  value: Are
- name: pronounCurrentTenseLower
  type: string
  description: The lowercase pronoun in the current tense
  value: are
- name: pronounPluralLower
  type: string
  description: The pronoun plural in lowercase
- name: pronounPossessive
  type: string
  description: The possessive pronoun
  value: Their
- name: pronounPossessiveLower
  type: string
  description: The possessive pronoun in lowercase
  value: their
- name: pronounSubject
  type: string
  description: The pronoun subject
  value: They
- name: pronounSubjectLower
  type: string
  description: The pronoun subject in lowercase
  value: they
- name: pronounObject
  type: string
  description: The pronoun object
  value: Them
- name: pronounObjectLower
  type: string
  description: The pronoun object in lowercase
  value: them
- name: pronouns
  type: string
  description: The full pronouns from the user
  value: (They/Them)
- name: pronounLastCached
  type: DateTime
  description: The date and time when the pronouns where last cached
  value: "2024-03-02 13:00:47"
---

::warning
  If a user has not configured their pronouns on alejo.io, a single variable will be populated:<br>
  :icon{name=i-mdi-chevron-right} `userFound`{lang=cs}: `false`{lang=cs}
::

## Parameters
::field-group
  ::field{name="User Login" type=Text required}
    Twitch username of the user to fetch pronouns for
  ::

  ::field{name="Variable Prefix" type=Text}
    *Optional* prefix to append to the resulting variables, to allow multiple uses of this sub-action within a single action.

    For example, if variable prefix is `user-one`, the resulting variables would consist of `user-one.pronounObject`, `user-one.pronounSubject`, and so on.
  ::
::