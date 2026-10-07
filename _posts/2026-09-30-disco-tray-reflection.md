---
layout: post
title: Disco Tray Reflection 09-30
author: Chris Bell
---

## Disco Tray Reflection 09-30

This week, me and Dylan worked on adjusting our data model. We removed the PrescribedEvents table from the model, as we found that we could simply put these fields in the Prescription itself. Now, Event1 Notes, Event1 OtherPerson, Event2 Notes, Event2 Otherperson, etc is stored within the Prescription model. This saved a lot of time for us to start working and implementing features such as refill redirects and searhing.

For this upcoming week, we must focus on correctly redirecting from the Follow Up Week 4 page to the Prescription creation page while autofilling the Student Email and Prescriber Email fields with the inability to change these fields. This is essentially ensuring that on the submission of the week 4 follow up, and when the prescriber/admin chooses to refill this prescription, they are automatically directed to create a new prescription without any issues. We also must implement search features so the admin/prescribers can filter through their prescriptions, the students, and various activities/events.
