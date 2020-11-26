---
description: >-
  This page presents the features offered by the journal de bord
  single-page-application.
---

# Features

## Overview

In short, the application can be used by a learner driver to register its first rides in a _journal de bord_ \(I used the french term just because I got used to it, you can think of it as logbook\). An instance of a journal de bord contains informations related to the logged rides. It is mainly made of the following:

* An objective: this is a number of kilometers the user wants to reach. The goal is to motivate young drivers to take the road!
* A list of rides and for each of them, the driver can keep track of...
  * … the departure and arrival location;
  * … the departure and arrival time;
  * … the departure and arrival value of the used vehicle speedometer;
  * … a traffic condition indicator
  * … a comment, this can be used by the user to note how good he did during his ride!

## Rides management

When a new user registers to the application for the first time a new journal de bord is automatically created. Currently, it is not possible to create more than one journal.

* The user can start a new rid_e_.
* The user can cancel a started ride before finishing.
* The user can finish a started ride to add it in the journal the bord.
* The user can directly add a new ride into its journal using a complete form.
* The user can list its previous rides.
* The user can view the details of a previous rides.
* The user can define a number of kilometers objective.

## Statistics

The user should be able to understand some tendencies based on the journal. For instance:

* How many kilometers were driven each day/ week/ month \(line chart\);
* How close is he to the defined objective \(progress bar\)?
* What is the most visited location?
* What is the time the driver rides the most?

## Data management

The user is able to manage the data that he shared with the journal de bord project. It is possible to extract a journal in different file formats: JSON, CSV, or PDF.

{% hint style="danger" %}
Currently, the backend that need to support those features is not developed yet. Besides, the interface only shows option for the JSON and PDF file formats in the profile page.
{% endhint %}

