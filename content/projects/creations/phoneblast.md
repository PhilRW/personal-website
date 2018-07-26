---
title: Phoneblast
date: 2016-05-05
featured: false
description: Self-managing double-opt-in telephone voice message broadcasting system
tags:
- perl
- asterisk
- AGI
- bash
- SIP
- git
- GitHub
image: /images/asterisk.png
link: https://github.com/PhilRW/phoneblast-asterisk
fact: 
weight: 500
sitemap:
  priority: 0.8
---

Design theory is that users should be able to opt-in to a phone message broadcasting service given an access phone number and a PIN. Upon joining that system will issue them a one-time-use challenge PIN/password, call them back, and have them enter that password in order to be confirmed and added to the list. Users can broadcast messages to the rest of the list.

Project utilizes Asterisk and AGI to perform scripting functions. Flat files for easy backend database manipulation.