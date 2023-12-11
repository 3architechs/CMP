# Architecture Katas - Customer Management Platform

## Business Case:
A leading airline is striving to build a comprehensive Customer Management Platform solution that enables the foundation of data driven, customer centric organization. This platform should enable to manage customer information across the ticket booking platforms both online and agents, call centre , check in desks, customer affairs and services, in flight retail, lounges, chauffer driven services and baggage services

## Business Drivers / Current Challenges
 
- Poor customer experience
- Lack of customer insights
- Absence of customer's historical interactions/transactions
- Lack of automated service recovery options.
- Complex system landscape leading to cumbersome data privacy management

## Business Goals
- Create detailed and comprehensive customer profiles
- Couple with analytical tools to allow the airline to remain closely engaged with the customers
- Create a seamless travel/customer experience
- Build personalized and tailored interactions and offers
- Tailor a marketing campaign to specific profiles
- Drive the sale of ancillary products and services
- Proactive grievance management and service recovery
- Enhance customer satisfaction and fuel customer retention
- Increase revenue and profit.
 

## Architecture Vision
The architecture vision for this solution includes:
 
- Integration of all available pieces of customer data to create a holistic view of the customer.
- Utilize data as a differentiator to enhance and personalize the organization's offerings.
- Provide advanced data analytic tools that can uncover insights, identify patterns, predict outcomes, and generate recommendations.
- Create a solution utilizing the latest technology stacks that is interoperable and can scale to sustain business growth and adapt to organizational changes.
- Plan and provision application resources that are cost-efficient.
- Design application, hosting, and deployment methods to be cloud-agnostic.
- Implement automation processes on repetitive tasks to minimize errors and FastTrack time to market.
- Ensure a comprehensive Identity and access management framework.
- Comply with GDPR, preserve anonymity in compliance with privacy regulations.
- Conform to PCIDSS and other regulatory requirements.
- Provision comprehensive logging and auditing of all consumer data access and modifications.
- Create consistent, user-friendly, and intuitive UI designs to improve the user experience.
- Platform components should be designed to provide an omni-channel consistent brand experience.


## Architecture Principles
| SL                     | Name                                   | Description
| ---------------------- | -------------------------------------- |---------------------------------------------------------------------------------------- |
| 1                      |Future Proof	                           | Technology must be viable for our use not only today but also in the foreseeable future.|
| 2                      |Interoperability                        | Technology must be capable to work with other technologies in the landscape.            |
| 3                      |Maintainability	                        | Capability of Technology to 1)Support changes gracefully in existing solutions deployed in this technology 2)Support enterprise automated environment management and automated release management processes. If not, technologies should have alternatives to ensure seamless environment management and release management capabilities 3)Customisations done are supported and scalable with future releases            |
| 4                      |Abstraction                             | Where possible, the underlying complexity of any technology should be presented through higher levels of abstraction.                                                                                                                                      |
| 5                      |Portability	                            | Technology should be portable as much as possible at all levels. For example: 1)It should be possible to deploy in house as well as on the cloud etc. 2)Data handled or stored by any technology should be easily extracted.                             |
| 6                      |Choose Right Fit Solutions              | 1)Commercial-off-the-shelf (COTS) packages should be selected based on their fit to the identified functional and non-functional requirements. 2) Common use applications are preferred over custom solutions. 3)Platforms preferred over best of breed solutions.4)Adopt industry standard business process and integrations instead of Adapting the business process to prescribed standards                      |
| 7                      |Design for failure	                     | Solutions must be designed to ensure that the applications can fully or partially available and or recover from software or infrastructure failures.                                                                                                    |
| 8                      |Separation of Concerns                  | Solutions are divided into discrete software components which are autonomous in nature. |
| 9                      |Design to meet SLA	                     | It is important that solutions are designed and developed with non-functional requirements in mind to meet service levels agreements offered to our customers.                                                                                            |
| 10                     |Loosely coupled, interoperable integrations| Solutions share well-defined integration points, which are standards based, interoperable and loosely coupled.                                                                                                                                        |
| 11                     |Customer Centric Design                    | Every hardware and software solution should be designed to comply with universal design guidelines and where required accessibility requirements                                                                                                    |


## System Requirements

## Stakeholders
 
This section describes key stakeholders of the system and their architectural concerns.
 
- **SH-1: Contact Centre Agent**
  - Provides customer service with regard to flight and ancillary bookings, also handles calls related to service disruption.
 
- **SH-2: Airport Check-in Agent**
  - Provides customer service with regard to flight check-in, ancillary bookings, flight boarding and also handles passenger grievances related to service disruption.
 
- **SH-3: Marketing Manager**
  - Creates marketing campaigns and promotions.
 
- **SH-4: Data Privacy Officer**
  - Manages customer data privacy requirements for the Organization.
 
- **SH-5: Loyalty Manager**
  - Drives loyalty offers and new product development.
 
- **SH-6: Cabin Crew**
  - Provides service to customers inflight and also promotes in-flight sales.
 
- **SH-7: CMP Manager**
  - Configures rules and policies and drives requirements for enhancing the platform.
 
- **SH-8: Customer Affairs Executive**
  - Handles customer complaints and compensation.
 
- **SH-9: Data Analyst**
  - Consolidates data from various operational systems to construct a thorough customer 360 view and unearth insights about customers in order to enhance Average Revenue per Customer (ARPC).
 
- **SH-10: Inflight Retailer**
  - Creates suitable product bundles for cross-selling during in-flight retail.
 
- **SH-11: Cyber Security Operations Manager**
  - Ensures that there are no security breaches in the system.

### Business Requirements

## Customer Profile Management
 
- Detailed and comprehensive customer profiles that include 
  - Personal information
  - Travel history 
  - Preferences 
  - Past interactions.
 
- A centralized repository that aggregates and stores customer data from various touchpoints and systems
 
- Tools for segmenting customers based on various criteria such as 
  - Travel history
  - Preferences
  - Loyalty status.
 
- Personalization features to tailor interactions and offers to individual customers
 
- Capability to share profile data with strategic partners while preserving anonymity in compliance with privacy regulations, while also revealing essential insights into segments, preferences, and choices
 
 
## Customer Interaction Management
 
- Logs of all past interactions, including calls, emails, chats, and in-flight retail purchases, stored within customer profiles.
 
- A chronological timeline view of each customer's interactions and transactions, allowing for easy tracking and reference .
 
- Critical information from customer feedback data, into customer profiles, including :
  - Complaints,
  - Compliments,
  - Cases, and
  - Suggestions.
 
 
## Customer Order Management
 
- Capture and store customer preferences related to orders, such as :
  - Meal choices 
  - Seating preferences.
 
- Personalization of future orders based on customer preferences .
 
- Integration with customer support and complaint handling systems to address order-related issues promptly
 
 
## Compensation Management
 
- Automated Compensation calculation and processing based on rules and policies.
 
- Support for multiple compensation scenarios, including flight cancellation, delays, and baggage mishandling.
 
- Notifications regarding compensation resolutions.
 
## Case Management
 
- Case creation, prioritization, tracking, and updates.
 
- Case Assignment, Routing, and escalation capabilities.
 
- Customer Self-service capabilities.
 
- Notifications regarding case status and closures.
 
## Customer Analytics Capabilities
 
- Data collection mechanisms from all touchpoints to gather information on passenger interactions, preferences, and behaviors.
 
- Real-time data processing and analysis to provide timely insights and responses.
 
- Advanced analytics capabilities including machine learning, and predictive analytics.
 
- Sentiment analysis of customer feedback and social media mentions to gauge passenger satisfaction.
 
- Capability to envisage various actions that could be implemented for a specific customer and then choose the best possible option to implement.
 
 
## Easy to Use
 
- Intuitive, multi-channel and user-friendly interfaces for passengers, call center agents, check-in agents, cabin crew, service management, and retail staff.
 
- Simplified navigation and clear layouts to access customer profiles and historical data.
 
 
## Secured Platform
 
- Right authentication and authorization implemented.
 
- Supports RBAC & MFA (Multi-Factor Authentication).
 
- Sensitive data encrypted at rest and in transit.
 
- Conforms to GDPR, PCIDSS, and other regulatory requirements.
 
- Comprehensive logging and auditing of all customer data access and modifications.


## Assumptions
 
1. The Analytics and reporting module provides near real-time data analysis for up-to-the-minute insights into customer interactions and trends, largely reliant on the data received from source systems.
 
2. Businesses often have varying processes for handling customer cases, and the module should be a generic solution.
 
3. The enterprise data lake serves as a robust foundation for our advanced customer analytics, harmonizing a myriad of customer data sources to provide a panoramic 360-degree perspective on customer behaviors and preferences.
 
4. The CMP platform's user access needs will be efficiently addressed through a user-friendly, responsive web application, eliminating the necessity for a dedicated app and ensuring seamless accessibility for users across diverse devices and platforms.
 
5. The marketing platform operates as an external entity to the CMP platform system, allowing this platform to excel in its specialized functions. This segregation ensures streamlined maintenance, facilitates updates without disrupting CRM operations, and allows for the independent evolution of marketing strategies, ultimately optimizing overall performance.
 
6. The successful integration and utilization of the new Customer Management Platform within the organization will be contingent upon seamless and efficient data extraction, transformation, and loading (ETL) processes facilitated by the enterprise SnapLogic ETL/ELT platform.
 
7. The effectiveness of implementing and operating the new Customer Management Platform will depend on the smooth integration and efficient communication enabled by the Enterprise Message broker. This assumption envisions that the message bus will adeptly manage the real-time exchange of data and information between the CMP system and other interconnected enterprise applications.
   

## System context diagram

![System-Context](architecture-diagrams/C0-System-Context.jpg)


## Container diagram
![Container](architecture-diagrams/C1-Container.jpg)


## Component diagram - Preference and Consent Management

![Component](architecture-diagrams/C2-Component.jpg)


## Deployment Diagram

![Deployment](architecture-diagrams/Deployment.jpg)

|SL |Category|Description|
| ---------------- | -------------------------------------- |---------------------------------------------------------------------------------------- |
|1|Environments - The CMP instances will be deployed across multiple environments| 1. Production environment: a) The production environment provides live services to your user base. b) Tier 1 SLA. c) Deployed across several regions to provide redundancy and infrastructure fault tolerance. d) Processes numbers of transactions and requests based on the business requirement. 2.Development environment: a) Used for creating the application features. b) Limited number of users and data. 3.Test environments: a) Environment to test performance, conduct UAT related to new feature and backup and restore procedures.|
|2|Application Tiers| 1. Web Tier: a) Micro frontends will be created and deployed for each domain functionality e.g. Profile, Case management etc. b) Provides HTTPS content to the client. 2. Application Tier: a) Microservices will be created and deployed. 3. Database Tier: a) Consists of RDS databases. b) Backend services will interact with database to source data. c) Database will be deployed as active and standby. Active DB will replicate to standby.|
|3|General guidelines| 1. Separate CI/CD per micro frontend /microservice for build and deployment of each image. Pipelines will contain Quality and Security checks. 2. Services will be deployed on EKS. Deploy in anti affinity mode with autoscaling. 3. Each data centre should have sufficient capacity to be able to take the full application load in the event of any failure. In event of failure configure health checks for automated failover. Resources should be sufficient (CPU and memory) to match the application needs and these should be guaranteed. Ensure network policies are in place for pods/namespace. 4. Backups and disaster recovery drills will be carried out to ensure set RPO and RTO can be met.|
|4|Observability| 1. Service Request/Response logs will be collected, stored and utilized for troubleshooting by application support teams. Splunk will be used for infrastructure monitoring. AppD instrumentation will be done to monitor application health. Distributed tracing and logging will be required for issue debugging and analysis.|
|5|Edge Protection| WAF will be employed for edge security and traffic management|


## Integration Diagram
![Integration](architecture-diagrams/Integration.jpg)




## Domain and Data Architecture
![Data](architecture-diagrams/DataArchitecture.jpg)

|Sr|Category|Data element|Source|Destination|Information Classification|Data Format|Integration Method|Remarks|
|--|--------|-------|-----|----|-----|--|------|----|
|1|Profile|Unique Profile ID, Email address, Phone number, Title, Last name, First name, Middle name,  Loyalty Number, Loyalty status*,* Passport number, Nationality, Passport expiry, Gender, Address*,* Device details, browser details, location.|Loyalty, Channels, GDS, Partners|CMP|Sensitive data| | | |
|2|Preferences|Seat, meal, drink |Loyalty > EDH|CMP| | | |Customer Self service capabilities|
|3|Past Interactions|Calls, Emails, Chats |CC Voice Platform|CMP| | | | |
|5|Case Management|Complaints, Resolution, Status|Channels |CMP| | | | Case creation, prioritization, tracking and updates. Case Assignment, Routing, and escalation capabilities. Notifications regarding case status and closures|
|7|Compensation|Compensation history|Finance| | | | |Automated Compensation calculation and processing based on rules and policies. Notifications regarding compensation resolutions|
|10|Consent and Subscriptions|Related attributes| | | | | | |
|6|Suggestions and compliments|Related attributes| | | | | |chronological timeline view,|
|8|Travel Booked and Historical|PNR, Flight details (Flight number, Departure airport, Arrival airport , date of travel, class of travel), E-Ticket number, Status (On Time, No Show, Delay, Involuntary Rebooked), Gate Number, Date of travel, Bag Tag number|Mainframe > EDH| | | | | |
|9|Ancillary Booked and Historical|Ancillary Type, Ancillary related attributes, Status (Fulfilled, service disruption)|Mainframe > EDH| | | | | |
|4|Purchases|In flight purchases, EK websites purchases| | | | | |Personalization of future orders based on customer preferences.|
|11|Post Order|Shipment details, Invoice| | | | | | |
|12|Flight Segment forecast|Cabin, RBD, Load|Mainframe > EDH| | | | | |
|13|Business Rules|Rules|CMP|CMP| | | | |
|14|Knowledge Management|Knowledge articles and SOPs|KMS| | | | | |
|16|Profile|Unique Profile ID, Email address, Phone number, Title, Last name, First name, Middle name,  Loyalty Number, Loyalty status*,* Passport number, Nationality, Passport expiry, Gender, Address*,* Device details, browser details, location.|*CMP*|*Channels* | | | | |
|17|Preferences|Seat, meal, drink |*CMP*|*Channels* | | | | |
|18|Compensation|Compensation history|*CMP*|*Channels* | | | | |










## Architecture Decision Records

[**ADR 1 Fundamental Architecture ADR**](Architecture-Decision-Records/Fundamental-Architecture.md)

[**ADR 2 Authentication and authorisation ADR**](Architecture-Decision-Records/Authentication.md)

[**ADR 3 Dedicated Mobile App ADR**](Architecture-Decision-Records/DedicatedMobileApp-Requirement.md)

[**ADR 4 User Interface Technology  ADR**](Architecture-Decision-Records/USerInterface-technology.md)

[**ADR 5 Backend Technology ADR**](Architecture-Decision-Records/Backend-Microservices-Technology.md)

## Well Architected Framework Tracability


### Performance Efficiency
#### Measurements
- User transaction should respond within the set limits  at peak load
- Read  <= 700ms (end to end) for 98 percentile transactions.
- Writes <=1.2 secs (end to end) for 98 percentile transactions.
#### Solution
- The platform has leveraged Caching; this allows for data being quickly retrieved from cache memory, leading to reduced latency and faster response times for microservices.
- The platform has leveraged asynchronous messaging in the form of events.

### Availability
#### Measurements
- Platform components availability will be 99.95 %  end to end.
- Upgrades should take place with minimal down time
- Upgrades to application as well as infrastructure should take place with zero down time.
- Upgrades to database should have < 30mins down time
#### Solution
- Deployment in multiple availability zones for Resilience.
- Load balanced across deployments
  
### Scalability
#### Measurements
- System should be scalable to cater to sudden or projected growth in transactions eg. Peak periods
- Read  <= 700ms (end to end) for 98 percentile transactions.
- Writes <=1.2 secs (end to end) for 98 percentile transactions.
#### Solution
- The platform's microservices approach enhances scalability by enabling the independent development, deployment, and scaling of small, modular services.
- The CMP system employs load balancing to distribute incoming traffic efficiently, ensuring optimal performance and preventing any individual component from becoming overloaded.
- K8s autoscale dynamically adjusting the number of running instances or pods based on the current workload, ensuring optimal resource utilization and responsiveness to varying demand.
  
### Cost optimization
#### Measurements
- Ensure resources are provisioned in a cost effective manner and that they are optimally utilized.
#### Solution
- Application deployed in Kubernetes cluster with proper HPA configurations updated.
- Re-use of enterprise capabilities, wherever possible.
  
  
### Security
#### Measurements
- Compliance with GDPR including consent management, PCIDSS.
- Communication between components using HTTPS.
- Sensitive data should be encrypted at rest.
- Comprehensive authorisation and authentication mechanisms should be provisioned.
- RBAC, MFA and least privilege access.
- Comprehensive logging and auditing of all customer data access and modifications.
#### Solution
- Azure AD tokens for user authentication and Okta for machine-to-machine (M2M) authentication.
- Utilization of SSL/TLS protocols for data exchange.
- Access is granted to users, groups, and applications at a specific scope.
- Personal Data and Sensitive Data attributes is masked and stored in order to meet GDPR norms related to data privacy protection.
- Data retention policies in place for sensitive customer data.
