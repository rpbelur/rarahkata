# Business Requirements #

## Business Goal ##
Trouble with the Trouble ticket system for Penulitmate Electronics.

## Business Requirements ##
1. Ticket tracking system to make sure every ticket that is filed can be tracked from start to end.
2. Assigning the consultants with the right expertise to the right ticket. 
3. Consultants should be able to use their mobile device to search the knowledge base and also add their notes with pictures if required.
4. System is highly available so that the call center staff can enter tickets anytime.
5. System never goes down during upgrade. It should be possible to do rollover upgrade.

## Assumed Requirements ##
1. Customer should be able to file tickets on their own based on their id from the WebApp. 
2. Auditability/Trackability of the tickets.
3. Systems can be remotely fixed ? 

## Extensibility Requirements ##
1. The new system will replace the current system to start with.
2. The new system can be deployed in multiple regions to handle locality specific load.

## Architectural Requirements ##
Following are the Functional, Availability and Scalability requirements. 
| #     | Architectural Requirement | Based on BR |
| ----------- | ----------- | --------------|
| 1 | Reliable way to store and track ticket status | |
| 2 | Reliable way to assign tickets to experts |  |
| 3 | Reliable way to upgrade | |
| 4 | Scalable to handle spikes in the load | |
| 5 | Management of SysOPS Squad | 1 |
| 6 | Managing customers support plan | 2 |
| 7 | Billing the customer on Annual basis | 2 |
| 8 | Assigning the consultant with the related expertise for a given job | 3 |
| 9 | Mobile based Knowledge base access for consultants | 4 |
| 10 | Mobile support for ticket retrieval | 5 |
| 11 | Mobile based notes update support of the knowledge base | 6 |
| 12 | Survey Collection and updating survey | 7 |
| 13 | Report generation based on usage  

## References for Authentication ##
https://medium.com/cloudsail-io/aws-cognito-use-existing-users-database-with-custom-authentication-flow-920142884c08

https://stackoverflow.com/questions/32203610/how-to-integrate-uml-diagrams-into-gitlab-or-github



