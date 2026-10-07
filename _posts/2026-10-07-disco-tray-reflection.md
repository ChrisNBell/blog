---
layout: post
title: Disco Tray Reflection 09-23
author: Chris Bell
---

## Disco Tray Reflection 10-07

This week, we realized that our model did not consider all the required information to work and had to rescaffold/migrate the model once more. Before, we only had Student.cs, Prescriber.cs, Prescription.cs, Activities.cs, FollowUpWeek1.cs, and FollowUpWeek4.cs. Now, we must add in two different tables: Referral.cs and Appointment.cs.

Referral.cs is the initial form that considers who is making the referral for a particular student, a description of why the referral is being created, a boolean value considering the safety of the submitter of the referral, and the particular student themselves. In creating this referral, we need to create a student if they do not already belong to the database. Otherwise, we will grab that student's id and attach it to this referral.

Appointment.cs is a form that allows the admin to assign students to prescribers, allowing prescribers the ability to create prescriptions with these students. The Appointment.cs form considers a student's id, prescriber's id, and a description containing information about the student's needs. An appointment will be embedded within a prescription, which means it is redundant to have PrescriberID and StudentID directly in the Prescriber model, so it is now removed. We are currently working on rescaffolding and remigrating these aspects of the model, which will hopefully be completed by the end of this week.
