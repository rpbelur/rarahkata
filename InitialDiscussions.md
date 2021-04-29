# Significant Architectural Requirements #
 
 
## Personas ##
### Administrator (slide 84) ### 
* Maintains the internal users of the system
* list of experts ( skillset, location, availability )
* Billing for customers
   * automated email based on user's support requirement
   * automated billing support
* List of supported products, name-value pairs, etc.
 
### Customer ( Slide 85 ) ###
* Registration
   *   Customer profile
   *   Support Contracts
   *   Billing Info
* Raise Problem tickets
* Fill out Survey
 
### SysOps Squad Experts ( Slide 86 ) ###
*   Assigned Problem tickets
*   Fix problems based on the tickets.
*   Knowlege Base
   * Search for solutions
   * Notes about repairs. ( adding to knowledge base )
 
### Manager ( Slide 87 ) ###  
*   Ticket Operations
*   Report Generation about the problems & how it is handled.
 
## Analysis ##
* Data Tier - Data Layer
* Mid Tier -  Business processing -- API Layer / Caching
* Web Tier - Web Based
   * enhancement required -- Mobile --
 
* Web based / Call based + Introduce new Mobile based
 
Mobile based should be able to access
   - ticket details
   - knowlege base
   - allow adding data ( ? )
 
## Solution Approach1 ##
 
1. No changes to the Data Tier
   Introduce an abstraction layer.
 
2. Identify the microservices.
   REST APIs
 
3. Web App, Mobile App
   Web Authentication
   Mobile Authentication
 
   Phase 2 - depending on the performance impact, model the data tier & do data migration.
 
## Solution Approach 2 ##
 
1. Propose data tier changes.
   Introduce an abstraction layer.
 
2. Identify the microservices.
   REST APIs
 
3. Web App, Mobile App
   Web Authentication
  
   Phase 2 - Mobile App
 
## Discussion Points ##
* No technology is said, - there might be lot of table joins - RDBMS
* System is buggy - CP system is required.
* Replicated DB - HA & Scaling
* Single Master DB - All services write to the same instance of DB.
* Sharding might be required - depending on the size of the data.
*
 
Issue of tickets not showing up properly
* DB Issue ? Business logic issue?
* Loss of tickets
* Skill set matching problem.
* System is not available - availability issue - HA
* System freezing / hanging - system doesn't scale - scalability issue.
* Will there be spikes in demand - seasonal - ??
   * Are you running in your own data center or on Cloud
       * Running on Cloud - Kubernetes - autoscaling is configured.
       * Is there a need for scaling ?
 
## List of items to be done ##
* System Design
* List of Microservices
   * Customer Registration service
   * Expert Regisration Service
   * Ticket Management Service
   * Knowledge Based Management Service
   * Report Generation Service
   * Notification Service
       * Email Notification
       * Mobile SMS Notification
   * Queuing Service ( ? Some kind of Queueing - Kafka ? - Why do you need queueing or DB Queues. There should be a reason to not use DB queueing)
* DB Analysis
* Migration Plan
* Cost Analysis
* Observability ( Metering, monitoring)
* Tradeoffs
   * Deploy the servers in mulitple data centers - latency - to serve users of the same area.
   * Deploy the servers in a central location - let the central location take care of serving all customers? Which approach will be cheaper?
 
## Cloud Services to be used ##
EC2
Application Load Balancer
Amazon Cognito
SNS
Route53
S3 Buckets ??? -- why do we need this?
   * Store the invoices
   * Reports
   * Data archival
API Gateway
Queuing
Amazon DynamoDB - Knowledge Base Records.
   * How is knowledge base is created. Product, kind of repair, category
   * How do you identify a unique requirement?
       * Washing machine/ Dryer - problems
       * TV - LCD crack -
CloudFormation - Infrastructure as Code.
RDBMS - Postgresql ( Cheaper )
ElasticSearch  -- to search Knowledge base.
 
Network Traffic Optimization
