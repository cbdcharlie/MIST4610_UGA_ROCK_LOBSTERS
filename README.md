# MIST4610_UGA_ROCK_LOBSTERS

Team Name and Members - Rock Lobsters
- Charlie Davis
- Will Jenkins @willjenkins-glitch
- Brooks Ruehle @Brooks-Ruehle

Scenario Description: 

We created this data model to serve as a real estate customer relationship management system. It tracks all the interactions that happens betweens customers, sales representatives, and properties. The database that we created helps to manage things such as a customer lead, the showings of properties, any offers, contracts, or payments, as well as commission. It is aimed at real estate agencies, which helps them to streamline sales with customers. 

Data Model

 ![image](https://github.com/user-attachments/assets/f0c97308-65ba-498d-9271-5048fece976d)

 Explanation of the Data Model

 Our data model looks to capture what a base model real estate customer relationship management system would look like. The payment entity looks to keep track of the payments made by customers to the agency so that they know the amount they're making.

 Then there is the Customer entity which helps to keep track of what the Customers name, email and phone are. It helps to tie together the payment by the customer, the offer the customer makes, and the contract that is presented along with the offer.

 Next there is the Offer entity, where a customer can have many offers but an offer can only be tied to one customer. The offer helps to keep track of the amount of the offer along with the date that the customer offered up that contract.

 Next there is the Contract entity, which can help to keep track of the contract associated with an offer, hence the one to one relationship. In this specific entity it contains the price tied to the contract, as well as the start and end of that contract.

 The SalesRep entity helps to keep track of the representatives at a specific agency. The entity keeps track of the name of the person, the email of the person, along with phone number and office location. A sales representative can have many properties associated with them as long as they have many customers that they serve. They can also offer many showings for properties. And lastly, they can receive a lot of feedback based on how they did.

 The Lead entity helps to identify any potential leads that a customer has with a property. The lead entity identifies the lead level with a number. Lead has a one to one relationship with Property because a lead can only be associated with one property. A customer can have multiple leads with different properties. 

 The Feedback entity helps to identity any feedback received by a sales representative. The feedback entity can store the comments and ratings that are associated with each SalesRep. A sales representative can have multiple feedbacks but a feedback is tied to only one sales representative.

 The Property entity helps to keep track of the properties that are listed or have been listed, which shows the many to many relationship associated with the Prop_has_SalesRep entity and Property entity. The property entity can help to keep track of the address, city, state and price of the property while also being tied to a lead. A property is only associated with one lead. A property can have many showings. A sales representative can have many showings.

 The Showing entity keeps track of the date of the showing as well as the time. A sales representative can have many showings but a showing is only tied to one sales representative. A property can have many showings but a showing is only tied to one property.


Key Relationships

- Customer ↔ Lead (One-to-Many)
  - A customer can have multiple leads, reflecting different properties they are interested in. Each lead is associated with one specific customer, helping sales reps track potential buyers effectively.
- SalesRep ↔ Showing (One-to-Many)
  - A sales representative can conduct multiple showings. Each showing is assigned to one sales rep, which helps in organizing and managing property viewings.
- Property ↔ Lead (One-to-Many)
  - A property can generate multiple leads, as different customers may express interest in it. Each lead points to a specific property, facilitating targeted follow-ups by sales representatives.
- Customer ↔ Offer (One-to-Many)
  - A customer can make multiple offers on different properties. Each offer is linked to a specific customer, providing a clear record of negotiations and transactions.
- Offer ↔ Contract (One-to-One)
  - Each offer can lead to one contract if accepted. This relationship formalizes the agreement and captures essential details of the sale.
- Customer ↔ Payment (One-to-Many)
  - A customer can make multiple payments related to different offers or contracts. Each payment is linked to a specific customer, ensuring accurate tracking of financial transactions.
- SalesRep ↔ Feedback (One-to-Many)
  - A sales representative can receive multiple feedback entries from customers. Each feedback record is associated with one sales rep, helping assess performance and customer satisfaction.
- SalesRep ↔ SalesRep_has_Property (One-to-Many)
  - A sales representative can be responsible for multiple properties. Each property assignment is linked to one sales rep, which aids in managing commissions and responsibilities.
- Property ↔ SalesRep_has_Property (One-to-Many)
  - A property can be associated with multiple sales representatives, particularly if it is being handled by a team. Each property assignment is linked to a specific property, which aids in coordinating sales efforts.



Data Dictionary:

Payment

<img width="717" alt="Screenshot 2024-10-01 at 12 40 46 AM" src="https://github.com/user-attachments/assets/ff4ee415-aa3d-44ab-8897-1be4ea3fb8c9">



Customer

<img width="719" alt="Screenshot 2024-10-01 at 12 41 21 AM" src="https://github.com/user-attachments/assets/a3d79e0d-6f99-4e94-8d54-d181278a43f9">



Offer

<img width="720" alt="Screenshot 2024-10-01 at 12 41 40 AM" src="https://github.com/user-attachments/assets/a9e1411c-ff17-45ff-a248-ae75f1b63288">



Contract

<img width="720" alt="Screenshot 2024-10-01 at 12 41 58 AM" src="https://github.com/user-attachments/assets/11a311e1-67bc-4956-93fb-f94f16d9f35d">



Lead

<img width="718" alt="Screenshot 2024-10-01 at 12 42 24 AM" src="https://github.com/user-attachments/assets/f041707b-25aa-4e3a-b4c2-2c7fcc8c8e25">




Property

<img width="720" alt="Screenshot 2024-10-01 at 12 42 45 AM" src="https://github.com/user-attachments/assets/c82a385e-f216-4a12-87eb-a8e8edc5fe09">



SalesRep_has_Property

<img width="721" alt="Screenshot 2024-10-01 at 12 43 03 AM" src="https://github.com/user-attachments/assets/693ad444-12d3-4e47-9f0d-3dd97e62cd7e">



Showing

<img width="722" alt="Screenshot 2024-10-01 at 12 43 19 AM" src="https://github.com/user-attachments/assets/0151e3be-680d-43a8-a366-adeb9ac027a9">



SalesRep

<img width="721" alt="Screenshot 2024-10-01 at 12 43 38 AM" src="https://github.com/user-attachments/assets/f922f20d-57b5-43a0-8ee0-7aa0e6bbf25a">



Feedback

<img width="719" alt="Screenshot 2024-10-01 at 12 43 55 AM" src="https://github.com/user-attachments/assets/d51749bc-2f47-4903-8fb1-c7caa8bffd69">

Query1

<img width="712" alt="Screenshot 2024-10-01 at 1 31 23 AM" src="https://github.com/user-attachments/assets/00506765-fd0d-4cb5-b9cb-c83da035bbc8">

This query uses Property and Prop_has_SalesRep entity, joining the two tables. It then identifies the properties listed in Atlanta along with finding out if they are active. All the prices of these houses are averaged out then shown with the city, Atlanta.
