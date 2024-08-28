---
title: Thank You Sent
description: Trigger for a Fourthwall Thank You Sent
version: 0.2.4
variables:
  - name: fw.isTest
    type: boolean
    description: Whether it was a test notifications from FourthWall
  - name: fw.id
    type: string
    description: Id of "Thank You Sent" event
    value: ty_rDL4uaBSQ_SUcO9XfwuoNQ
  - name: fw.shopId
    type: string
    description: Id of the shop
    value: sh_97ff673d-f81d-49b2-a844-bdd12a7002fb
  - name: fw.mediaUrl
    type: string
    description: Media URL which was attached to the Thank You message
    value: https://fourthwall.com/video
  - name: fw.username
    type: string
    description: Name of the user the message was sent to
    value: John Doe
 - name: fw.email
    type: string
    description: E-mail adress of user. Please be careful how this is used.
    value: john.doe@gmail.com
  - name: fw.message
    type: string
    description: Message that was being sent
    value: Thank you for your support!
  - name: fw.type
    type: string
    description: Type of "Thank You Sent"
    value: ORDER, DONATION, GIFT_PURCHASE
---
