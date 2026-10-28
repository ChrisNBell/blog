---
layout: post
title: Disco Tray Reflection 10-14
author: Chris Bell
---

## Disco Tray Reflection 10-14

This week, me and Dylan fixed the Follow Up Week 4 to Prescription redirect. We needed to pass an appointment id from the context of Appointment into Prescription upon creation of the week 4 follow up. If the appointment id is not null or 0, then there is a particular appointment we are referring to, and therefore, this field needs to be autofilled. We currently have the appointment number and the student's email as the autofill value. This ensures the prescriber can see which appointment is being referred to upon redirect, allowing for fluency within our model.

The next steps are to fix up the redirect from a prescriber's appointments page to the creation of the prescription for that appointment. There are also many fields in details that are empty currently, which need to be updated in order to see the relevant information. This will allow the admin to be able to see specific information about students and prescribers, and prescribers and admins can see information about specific appointments and referrals.
