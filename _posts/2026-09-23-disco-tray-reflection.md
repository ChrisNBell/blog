---
layout: post
title: Disco Tray Reflection 09-23
author: Chris Bell
---

## Disco Tray Reflection 09-23

This week, me and Dylan worked on implementing the complex data model. First, we had to correctly assign foreign keys to each respective table, making sure the Prescription model was connected to the Student, Prescribed Events, and Prescriber models. We ran into problems early in creating a Prescription, as we were unable to view the available activities to choose from. We then altered the Prescription create page to fix this error, and we can now choose from any activity that is created in the Activity model.

We then ran into a lot of errors when attempting to create Prescribed Events from the Prescription create page. Initially, our keys were invalid, so we re-migrated and re-scaffolded the entire model with no underscores and corrected ID names. This issue was fixed shortly after doing so. The next step was creating the Prescribed Events, in which we succcessfully created the Prescribed Events from the Prescription table and re-inserted them back into the Prescription, in which each Prescribed Event is unique to a specific Prescription. Now, we must fix the FollowUpWeek4 model to autofill the Prescription create page after clicking "refill" in the create page for FollowUpWeek4 model. We also need to change the status of the Prescription to archived. s
