# Business Requirements #

## Business Goal ##
Trouble with the Trouble ticket system for Penulitmate Electronics.

## Business Requirements ##
1. Assigning the consultants with the right expertise to the right job. Making sure the ticket assignment process is correct.
2. Ticket tracking system to make sure every ticket that is filed can be tracked from start to end.
3. Experts should be able to use their mobile device to search the knowledge base and also add their notes with pictures if required.
4. System is highly available so that the call center staff can enter tickets anytime.
5. System never goes down for upgrade.

## Assumed Requirements ##
1. Customer should be able to file tickets on their own based on their id.
2. Auditability/Trackability of the tickets.
3. Systems can be remotely fixed ? 

## Architectural Requirements ##
| #     | Architectural Requirement | Based on BR |
| ----------- | ----------- | --------------|
| 1 | Reliable way to store and track ticket status | |
| 2 | Reliable way to assign tickets to experts |  |
| 3 | Reliable way to upgrade | |
| 4 | Easy to scale | |
| 5 | Management of SysOPS Squad | 1 |
| 6 | Managing customers support plan | 2 |
| 7 | Billing the customer on Annual basis | 2 |
| 8 | Assigning the consultant with the related expertise for a given job | 3 |
| 9 | Mobile based Knowledge base access for consultants | 4 |
| 10 | Mobile support for ticket retrieval | 5 |
| 10 | Mobile based notes update support of the knowledge base | 6 |
| 11 | Survey Notification | 7 |



## References for Authentication ##
https://medium.com/cloudsail-io/aws-cognito-use-existing-users-database-with-custom-authentication-flow-920142884c08

https://stackoverflow.com/questions/32203610/how-to-integrate-uml-diagrams-into-gitlab-or-github



