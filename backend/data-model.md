# Data Model

![](https://lh5.googleusercontent.com/CJbRFys1CdjCoJXRX_G2TDuGGGaJXZEDLEbkdMMrXD17A8ZarR_o9KlGosyCkCDBE3g8HX9-9LrHa9GzouZMdL8xBIvCcSVltGtpf7Vne4UedU_Q4jIOtfogau1aFb7Kcc8ogFWw)

[**Connect a Spring Boot application to Heroku Postgres**](https://stackoverflow.com/questions/33633243/connecting-to-heroku-postgres-from-spring-boot)

### **Constraints**

* Ride: the departure and arrival stops should never be equal for an entity.
* Ride: traffic condition should be an enumeration \(5 levels\)
* A location name should be unique in the set of a driver locations
* The departure of a ride should be before arrival

