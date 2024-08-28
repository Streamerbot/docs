---
title: Newsletter Subscribed
description: Trigger for a user subscribing to your newsletter on Fourthwall
version: 0.2.4
variables:
  - name: fw.isTest
    type: boolean
    description: Whether it was a test notifications from FourthWall
  - name: fw.createdAt
    type: DateTime
    description: DateTime of when a user subscribed to the newsletter
  - name: fw.shopId
    type: string
    description: Id of the shop
    value: sh_97ff673d-f81d-49b2-a844-bdd12a7002fb
 - name: fw.email
    type: string
    description: E-mail adress of user. Please be careful how this is used.
    value: test@email.com
---
