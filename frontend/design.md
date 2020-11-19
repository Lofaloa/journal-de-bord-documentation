---
description: >-
  This section describes the mobile user interface. The objective is to
  understand the interface pages and components. This covers their design and
  their purpose.
---

# Mobile User Interface

## **Introduction**

The section explains some design and functional choices from a high level. The objective isn't to dive in the code. It is to review the different application pages and components so that the reader understand their purpose and usage. Some design choices may be explained in this section as well. 

## **Home page**

The home page is the heart of the user interface. This pages has two roles. On one hand, it gives a quick overview of the journal to the driver. The progress overview card shows how close to the objective the driver is. And the Recent rides card shows the three last completed rides. On the other hand, the controller card offers control to the user that make it possible to start, finish and cancel the tracking of a ride.

## Profile page

The should be used by the user for simple configuration and data manipulation tasks. At the very least, he should be able to edit its distance \(kilometers\) objective, export a journal, and delete a journal.

## **Rides page**

### **Form**

* Global rules
  * The departure should be before the arrival \(when done\).
  * The departure odometer should be smaller than the arrival odometer \(when done\).
  * When a ride isn’t done it shouldn’t have an arrival value, it should be null.
* Fields:
  * Departure:
    * Odometer: positive integer, required.
    * Moment: date and time, required
    * Location: required
  * Arrival: the arrival is nullable. When it is null, the ride isn’t done yet.
    * Odometer: positive integer, required
    * Moment: required
    * Location: required
  * Retrospective:
    * Traffic condition: required, integer
    * Comment: characters string \(255\), not blank, nullable

{% embed url="https://formik.org/" %}

### **Rides list**

The mobile version of the app should be simple. Complexe pagination should be avoided.

A good option would be to add a “load more” button. We could load like 10 items at the time. Each time the user clicks the “load more” button, 10 new items are loaded and shown on the screen.

[**https://ux.stackexchange.com/questions/22521/best-table-pagination-pattern-for-a-mobile-browser-experience**](https://ux.stackexchange.com/questions/22521/best-table-pagination-pattern-for-a-mobile-browser-experience)

## **Resources**

{% embed url="https://material-ui.com/getting-started/installation/" %}

  


