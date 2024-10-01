# MIST4610_UGA_ROCK_LOBSTERS

Team Name and Members: Rock Lobsters
Charlie Davis
Will Jenkins
Brooks Ruehle

Scenario Description: 
We created this data model to serve as a real estate customer relationship management system. It tracks all the interactions that happens betweens customers, sales representatives, and properties. The database that we created helps to manage things such as a customer lead, the showings of properties, any offers, contracts, or payments, as well as commission. It is aimed at real estate agencies, which helps them to streamline sales with customers. 


Data Dictionary:

Payment
- idPayment
- date
- amount
- idCustomer

Customer
- idCustomer
- name
- email
- phone

Offer
- idOffer
- date
- amount
- idCustomer

Contract
- idContract
- start
- end
- totalPrice
- idOffer

Lead
- idLead
- interestLevel
- idProperty
- idCustomer

Property
- idProperty
- address
- city
- state
- price

SalesRep_has_Property
- idSalesRep
- idProperty
- status
- commissionPercent

Showing
- idShowing
- date
- time
- idSalesRep
- idProperty

SalesRep
- idSalesRep
- name
- email
- phone
- officeLocation

Feedback
- idFeedback
- comments
- rating
- idSalesRep
