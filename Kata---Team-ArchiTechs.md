

# Architecture Katas:

** Business Case **
A leading airline is striving to build a comprehensive Customer Management Platform solution that enables the foundation of data driven, customer centric organization. This platform should enable to manage customer information across the ticket booking platforms both online and agents, call centre , check in desks, customer affairs and services, in flight retail, lounges, chauffer driven services and baggage services



 **Business Drivers / Current Challenges** 
* Poor customer experience
* Lack of customer insights
* Absence of customer's historical interactions/transactions
* Lack of automated service recovery options.
* Complex system landscape leading to cumbersome data privacy management

 **Business Goals** 
1. Create detailed and comprehensive customer profiles
1. Coupled with analytical tools, allow airline to remain closely engaged with the customers
1.  Create a seamless travel/customer experience. 
1. Build personalized and tailored interactions and offers.
1. Tailor a marketing campaign to specific profiles.
1. Drive the sale of ancillary products and services.
1. Proactive grievance management and service recovery.
1. Enhance customer satisfaction and fuel customer retention.
1. Increase revenue and profit.

 **Architecture Vision**  
 
 The architecture vision  for this solution.


1. Integration of all available pieces of customer data to create a holistic view of the customer.
1. Utilise data as a differentiator to enhance and personalize the organisations offerings
1. Provide advanced data analytic tools that can be used to uncover insights, identify patterns, predict outcomes, and generate recommendations.
1. Create a solution utilizing latest technology stacks that is interoperable and can scale in order to sustain the business growth and adapt to organisation changes.
1. Plan and provision application resources that are cost efficient.
1. Design application, hosting and deployment methods will be cloud agnostic. 
1. Implement automation processes on repetitive tasks to minimise error and in order to FastTrack time to market
1. Ensure comprehensive Identity and access management framework.
1. Comply with GDPR, preserve anonymity in compliance with privacy regulations
1. Conform to PCIDSS and other regulatory requirements.
1. Provision comprehensive logging and auditing of all consumer data access and modifications.
1. Create consistent, user friendly and intuitive UI designs to improve user experience.
1. Platform components should be designed to provide a omni channel consistent brand experience.



 **Architecture Principles** 

| Sr# | Name | Description | 
|  --- |  --- |  --- | 
| 1 |  **Future Proof**  | Technology must be viable for our use not only today but also in the foreseeable future. | 
| 2 |  **Interoperability**  |  Technology must be capable to work with other technologies in the landscape. | 
| 3 |  **Maintainability**  | Capability of Technology to<ul><li>Support changes gracefully in existing solutions deployed in this technology</li><li>Support enterprise automated environment management and automated release management processes. If not, technologies should have alternatives to ensure seamless environment management and release management capabilities</li><li>Customisations done are supported and scalable with future releases</li></ul> | 
| 4 |  **Abstraction**  | Where possible, the underlying complexity of any technology should be presented through higher levels of abstraction. | 
| 5 |  **Portability**  | Technology should be portable as much as possible at all levels.For example:<ul><li>It should be possible to deploy in house as well as on the cloud etc.</li><li>Data handled or stored by any technology should be easily extracted.</li></ul> | 
| 6 |  **Choose Right Fit Solutions**  | <ul><li>Commercial-off-the-shelf (COTS) packages should be selected based on their fit to the identified functional and non-functional requirements.</li><li>Common use applications are preferred over custom solutions</li><li>Platforms preferred over best of breed solutions.</li><li>Adopt industry standard business process and integrations instead of Adapting the business process to prescribed standards</li></ul> | 
| 7 |  **Design**  ** for failure**  | Solutions must be designed to ensure that the applications can fully or partially available and or recover from software or infrastructure failures. | 
| 8 |  **Separation of Concerns**  | Solutions are divided into discrete software components which are autonomous in nature. | 
| 9 |  **Design to meet SLA**  | It is important that solutions are designed and developed with non-functional requirements in mind to meet service levels agreements offered to our customers.  | 
| 10 |  **Loosely coupled, interoperable integrations**   | Solutions share well-defined integration points, which are standards based, interoperable and loosely coupled. | 
| 11 |  **Customer Centric Design **  | Every hardware and software solution should be designed to comply with universal design guidelines and where required accessibility requirements | 


 **System Requirements** 

Stakeholders

This section describes key stakeholders of the system and their architectural concerns.


* 
    *  **SH-1** :  **Contact Centre Agent** (security)


    * Provides customer service with regard to flight and ancillary bookings, also handles calls related to service disruption.

    
    *  **SH-2** :  **Airport Check-in Agent** (availability, performance, scalability, robustness)


    * Provides customer service with regard to flight check-in, ancillary bookings, flight boarding and also handles passenger greviences related to service disruption.

    
    *  **SH-3** :  **Marketing Manager** (availability, performance)


    * Creates marketing campaigns and promotions.

    
    *  **SH-4** :  **Data Privacy Officer** (reportability)


    * Manages customer data privacy requirements for the Organisation.

    
    *  **SH-5** : **Loyalty Manager**  (availability, performance)


    * Drives loyalty offers and new product development.

    
    *  **SH-6** : **Cabin Crew**  (extensibility)


    * Provides service to customers inflight and also promotes inflight sales.

    

    


* 
    *  **SH-7: CMP Manager**  (extensibility)


    * Configures rules and policies and drives requirements for enhancing the platform

    
    *  **SH-8: Customer Affairs Executive**  (extensibility)


    * Handles customer complaints and compensation.

    
    *  **SH-9: Data Analyst**  (extensibility)


    * Consolidates data from various operational systems to construct a thorough customer 360 view and unearth insights about customers in order to enhance Average Revenue per Customer

    (ARPC).

    
    *  **SH-10: Inflight Retailer**  (extensibility)


    * Creates suitable product bundles for cross-selling during in-flight retail.

    
    *  **SH-11: Cyber Security Operations Manager** 
    * Ensures that there are no security breaches in the system

    

    



Business Requirements

_____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________







| Sr# | Capability | Key Business Requirements | 
|  --- |  --- |  --- | 
| 1 | Customer Profile Management | 
1. Detailed and comprehensive customer profiles that include ( **BR - 01)** 
    1. Personal information
    1. Travel history 
    1. Preferences 
    1. Past interactions.

    
1. A centralized repository that aggregates and stores customer data from various touchpoints and systems. **(EN - 01)** 
1. Tools for segmenting customers based on various criteria such as  **(BR - )**  
    1. Travel history
    1. Preferences
    1. Loyalty status. 

    
1. Personalization features to tailor interactions and offers to individual  customers.  **(BR - )**  
1. Capability to share profile data with strategic partners while preserving anonymity in compliance with privacy regulations, while also revealing essential insights into segments, preferences, and choices.  **(BR - )**  

 | 
| 2 | Customer Interaction Management | 
1. Logs of all past interactions, including calls, emails, chats, and in-flight retail purchases, stored within customer profiles.  **(BR - )**  
1. A chronological timeline view of each customer's interactions and transactions, allowing for easy tracking and reference.  **(BR - )**  
1. Critical information from customer feedback data, into customer profiles, including  **(BR - )**  
    1. Complaints,
    1. Compliments,
    1. Cases and
    1. Suggestions

    

 | 
| 3 | Customer Order Management | 
1. Capture and store customer preferences related to orders, such as  **(BR - )** 
    1. Meal choices 
    1. Seating preferences.

    
1. Personalization of future orders based on customer preferences.  **(BR - )** 
1. Integration with customer support and complaint handling systems to address order related issues promptly.  **(BR - )** 

 | 
| 4 | Compensation Management | • Automated Compensation calculation and processing based on rules and policies • Support for multiple compensation scenarios, flight cancellation, delays, and baggage mishandling. •Notifications regarding compensation resolutions | 
| 5 | Case Management | • Case creation, prioritization, tracking and updates. • Case Assignment, Routing, and escalation capabilities • Customer Self service capabilities •Notifications regarding case status and closures | 
| 6 | Customer Analytics Capabilities | • Data collection mechanisms from all the touchpoints to gather information on passenger interactions, preferences, and behaviours. • Real-time data processing and analysis to provide timely insights and responses • Advanced analytics capabilities including machine learning, and predictive analytics. • Sentiment analysis of customer feedback and social media mentions to gauge passenger satisfaction • Capability to envisages various actions that could be implemented for a specific customer and then chooses the best possible option to implement | 
| 7 | NFR  - Easy to Use | • Intuitive, multi-channel and user-friendly interfaces for passengers, call center agents, check-in agents, cabin crew, service management and retail staff. • Simplified navigation and clear layouts to access customer profiles and historical data. | 
| 8 | NFR - Secured Platform | • Right authentication and authorization implemented • Supports RBAC & MFA • Sensitive data encrypted at rest and transit • Conforms to GDPR, PCIDSS and other regulatory requirements. • Comprehensive logging and auditing of all customer data access and modifications. | 





        



 **Constraints**  **Assumptions** 
* The Analytics and reporting module provides near real-time data analysis for up-to-the-minute insights into customer interactions and trends which is largely reliant on the data received from source systems.
* Businesses often have varying processes for handling customer cases, and the module should would be a generic 
* The enterprise data lake serves as a robust foundation for our advanced customer analytics , harmonizing a myriad of customer data sources to provide a panoramic 360-degree perspective on customer behaviours and preferences.
* The CMP platform's user access needs will be efficiently addressed through a user-friendly, responsive web application, eliminating the necessity for a dedicated app and ensuring seamless accessibility for users across diverse devices and platforms.
* The marketing platform as an external entity to the CMP platform system allowing this platform to excel in its specialized functions. This segregation ensures streamlined maintenance, facilitates updates without disrupting CRM operations, and allows for the independent evolution of marketing strategies, ultimately optimizing overall performance.
* The successful integration and utilization of the new CMP platform within the organization will be contingent upon seamless and efficient data extraction, transformation, and loading (ETL) processes facilitated by the enterprise SnapLogic ETL/ELT platform.
* The effectiveness of implementing and operating the new CMP platform will depend on the smooth integration and efficient communication enabled by the Enterprise Message broker . This assumption envisions that the message bus will adeptly manage the real-time exchange of data and information between the CMP system and other interconnected enterprise applications.



 **Baseline Architecture** 



 **Target Architecture** 

        Use Case Model

             The following diagram shows mapping of architecture characteristics requirements on the key use cases based on requirements:

    



 **Logical Architecture** 320cbc10-b6b0-46c6-8776-1bcc261bddccLOGICALLOGICAL16



 **System context diagram** 

trueSY_CO_KAT_ArchTecSY_CO_KAT_ArchTec61









 **Container diagram** f1b45b51-0f52-4171-830d-ce8d77d5aea2CMP Container FE and BECMP Container Backend9



 **Component diagram - Preference and Consent Management** 

ee28bcae-f636-44cb-b2df-256c40108f87Case Comp-CMPCase Comp-CMP3





         Deployment



1200CMPDeployCMPDeploy1


## Integration




 **1200CMP IntegrationCMP Integration2** 













 **Domain and Data Architecture** Please capture the main data assets used by the initiative and their relationships. A sample model is presented below. When the further details become available, the model can be elaborated to a logical level. Please note the model is at the  **conceptual level** .





1200Data ArchData Arch5





| Sr# | Category | Data element | Source | Destination | Information Classification | Data Format | Integration Method | Remarks | 
|  --- |  --- |  --- |  --- |  --- |  --- |  --- |  --- |  --- | 
| 1 | Profile | Unique Profile ID, Email address, Phone number, Title, Last name, First name, Middle name,  Loyalty Number, Loyalty status **,** Passport number, Nationality, Passport expiry, Gender, Address **,** Device details, browser details, location. | LoyaltyChannelsGDSPartners | CMP | Sensitive data |  |  |  | 
| 2 | Preferences | Seat, meal, drink  | Loyalty > EDH | CMP |  |  |  | Customer Self service capabilities | 
| 3 | Past Interactions | Calls, Emails, Chats  | CC Voice Platform | CMP |  |  |  |  | 
| 5 | Case Management | Complaints, Resolution, Status | Channels  | CMP |  |  |  |  Case creation, prioritization, tracking and updates. Case Assignment, Routing, and escalation capabilities. Notifications regarding case status and closures | 
| 7 | Compensation | Compensation history | Finance |  |  |  |  | Automated Compensation calculation and processing based on rules and policies. Notifications regarding compensation resolutions | 
| 10 | Consent and Subscriptions | Related attributes |  |  |  |  |  |  | 
| 6 | Suggestions and compliments | Related attributes |  |  |  |  |  | chronological timeline view, | 
| 8 | Travel Booked and Historical | PNR, Flight details (Flight number, Departure airport, Arrival airport , date of travel, class of travel), E-Ticket number, Status (On Time, No Show, Delay, Involuntary Rebooked), Gate Number, Date of travel, Bag Tag number | Mainframe > EDH |  |  |  |  |  | 
| 9 | Ancillary Booked and Historical | Ancillary Type, Ancillary related attributes, Status (Fulfilled, service disruption) | Mainframe > EDH |  |  |  |  |  | 
| 4 | Purchases | In flight purchases, EK websites purchases |  |  |  |  |  | Personalization of future orders based on customer preferences. | 
| 11 | Post Order | Shipment details, Invoice |  |  |  |  |  |  | 
| 12 | Flight Segment forecast | Cabin, RBD, Load | Mainframe > EDH |  |  |  |  |  | 
| 13 | Business Rules | Rules | CMP | CMP |  |  |  |  | 
| 14 | Knowledge Management | Knowledge articles and SOPs | KMS |  |  |  |  |  | 
| 16 | Profile | Unique Profile ID, Email address, Phone number, Title, Last name, First name, Middle name,  Loyalty Number, Loyalty status **,** Passport number, Nationality, Passport expiry, Gender, Address **,** Device details, browser details, location. |  **CMP**  |  **Channels **  |  |  |  |  | 
| 17 | Preferences | Seat, meal, drink  |  **CMP**  |  **Channels **  |  |  |  |  | 
| 18 | Compensation | Compensation history |  **CMP**  |  **Channels **  |  |  |  |  | 



Security:

1200CMS SecurityCMS Security4





 **Architecture Decision Records** Key decisions taken for the implementation of the interfaces:



| Decision on Fundamental Architecture Style | Fundamental Architectural Design
### Context
Our organization is in the process of designing a new Customer Management Platform (CMP) system, and we need to make a decision on the architectural design for same. This decision is crucial as it will significantly impact the scalability, maintainability, and flexibility of the system.

 **Status** Accepted


### Decision-Making Process
To guide our decision-making process, we will leverage the "Architecture Styles Worksheet" introduced by Mark Richards, available at [https://www.developertoarchitect.com/resources.html](https://www.developertoarchitect.com/resources.html). This worksheet provides a systematic approach to evaluating key architectural characteristics and selecting the most suitable architecture style for our project.


### Key Architectural Characteristics
We have identified the following key architectural characteristics that are essential for the success of the new CMP platform:


1.  **Scalability:**  The ability to handle a growing number of users, data, and transactions efficiently.


1.  **Maintainability:**  Ease of maintaining, updating, and evolving the system over time.


1.  **Flexibility:**  The ability to adapt to changing business requirements and integrate with other systems.


1.  **Resilience:**  The ability to recover gracefully from failures and ensure high availability.


1.  **Speed of Delivery:**  Rapid development and deployment of new features and updates.





Prior to immersing ourselves in the architecture design phase, it is crucial that we establish a unanimous agreement on the foundational architectural style for our system. This choice bears considerable importance, as making adjustments later in the process could incur significant costs. Hence, this stands as our initial decision in the process

To facilitate this decision-making process, we are leveraging an "Architecture Styles Worksheet" introduced by Mark Richards, available at [https://www.developertoarchitect.com/resources.html](https://www.developertoarchitect.com/resources.html).

![](images/storage/image-2023-12-8_11-14-16.png)


### Architecture Styles Evaluation
We will evaluate the following architecture styles using the provided worksheet:


1.  **Monolithic Architecture** 
1.  **Microservices Architecture** 
1.  **Service-Oriented Architecture (SOA)** 
1.  **Event-Driven Architecture** 


### Decision
After a thorough evaluation based on the Architecture Styles Worksheet, we have decided to favor the  **Microservices Architecture**  for the new CMP platform.

Rationale
1.  **Scalability:**  Microservices architecture allows for independent scaling of services, enabling us to scale specific components based on demand.


1.  **Maintainability:**  With microservices, each service can be developed, deployed, and maintained independently, facilitating easier maintenance and updates without affecting the entire system.


1.  **Flexibility:**  Microservices provide the flexibility to choose the right technology stack for each service, facilitating easier integration with other systems and adaptability to changing business requirements.


1.  **Fault tolerance & Resilience:**  Isolation of services in microservices architecture ensures that a failure in one service does not bring down the entire system, contributing to overall system resilience.


1.  **Speed of Delivery:**  Microservices enable faster development cycles, allowing us to deliver new features and updates more rapidly.




### Implications

1.  **Organizational Change:**  Adopting microservices may require a shift in organizational culture and processes to align with the decentralized nature of microservices development.


1.  **Operational Complexity:**  Managing a microservices-based system introduces challenges in terms of operational complexity, monitoring, and orchestration.



 | 
| User Onboarding and Authentication Strategy | User Onboarding and AUTH Strategy
### Context
The need for a robust User Onboarding and Authentication Strategy has been identified for our system. User authentication is a critical aspect of the application, and a combination of Azure AD tokens and Okta is proposed to address the requirements.


### Status
Accepted


### Decision
The decision is to employ Azure AD tokens for user authentication and Okta for machine-to-machine (M2M) authentication.


### Rationale

1.  **Azure AD Token for User Authentication:** 

<ul><li>Azure AD is a widely-used identity and access management service that provides secure and seamless user authentication.</li><li>Leveraging Azure AD tokens ensures compliance with industry standards and best practices for user authentication.</li><li>Azure AD supports a variety of authentication methods, including multi-factor authentication (MFA), enhancing the overall security posture of the application.</li></ul>
1.  **Okta for Machine-to-Machine (M2M) Authentication:** 

<ul><li>Okta is well-suited for M2M authentication, providing a scalable and secure solution for interactions between machines or services.</li><li>Okta offers robust APIs and integration capabilities, allowing for seamless integration with various machine-driven processes within the system.</li><li>This separation of user and machine authentication helps manage access controls more effectively and enhances the overall security of the system.</li></ul>


### Alternatives Considered

1.  **Using Azure AD for Both User and Machine Authentication:** 

<ul><li>While Azure AD supports M2M authentication scenarios, introducing Okta for this purpose provides a specialized solution tailored for machine-driven processes.</li><li>Okta's specific focus on M2M interactions may lead to better performance and scalability in scenarios involving numerous machine-authenticated requests.</li></ul>
1.  **Choosing an Alternative M2M Authentication Provider:** 

<ul><li>Considered other identity providers for M2M authentication, but Okta was selected based on its reputation, feature set, and proven track record in not just airline but also with financial institutions like S&P , Nasdaq. </li></ul>


### Implications

1.  **Integration Effort:** 

<ul><li>Development teams need to integrate both Azure AD and Okta into the system. Proper documentation and support will be essential to facilitate a smooth integration process.</li></ul>
1.  **Maintenance and Support:** 

<ul><li>Teams responsible for maintaining the authentication components should be familiar with both Azure AD and Okta, necessitating appropriate training and documentation.</li></ul>
1.  **Cost Considerations:** 

<ul><li>Evaluate the cost implications of using both Azure AD and Okta. While Azure AD may be part of existing subscriptions, Okta's cost should be factored into the overall budget.</li></ul>
1.  **Security Monitoring:** 

<ul><li>Implement a comprehensive security monitoring solution to track user and machine authentication events, ensuring timely detection of any suspicious activities.</li></ul>



 | 
| Java with Spring Boot for the backend API development | Server Side stack  **Context:** The system requires a robust and scalable architecture, and the decision has been made to use Java with Spring Boot for the backend API development.

 **Decision:** The chosen architecture for the Customer Management Platform System includes Java as the programming language and Spring Boot as the framework for developing the backend API.

 **Status:** Accepted


### Rationale:

### 1.  **Scalability:** 
<ul><li> **Pro:**  Java, known for its scalability, will enable the system to handle a large number of concurrent users and scale seamlessly as the customer base grows.</li><li> **Con:**  Initial development may take slightly longer due to the statically typed nature of Java, but the long-term benefits in terms of performance and scalability justify this decision.</li></ul>
### 2.  **Community Support:** 
<ul><li> **Pro:**  Java and Spring Boot have extensive community support, which ensures that the development team can find solutions to problems quickly and benefit from a wealth of resources.</li><li> **Con:**  Depending on the specific requirements, some niche features might have less community support compared to other languages or frameworks.</li></ul>
### 3.  **Development Speed:** 
<ul><li> **Pro:**  Spring Boot's convention-over-configuration approach speeds up development, allowing developers to focus on business logic rather than boilerplate code.</li><li> **Con:**  There might be a learning curve for developers who are not familiar with Java or Spring Boot, but the abundance of tutorials ,documentation and recent advent of AI assisted coding  can mitigate this.</li></ul>
### 4.  **Integration Capabilities:** 
<ul><li> **Pro:**  Java and Spring Boot provide excellent support for integration(tried and tested) with various databases, messaging systems, and other third-party services, ensuring seamless connectivity with other enterprise systems.</li><li> **Con:**  Ensuring proper integration might require additional effort in terms of configuration and testing.</li></ul>
### 5.  **Security:** 
<ul><li> **Pro:**  Java has a strong focus on security, and Spring Boot provides features such as built-in support for HTTPS, libraries for secure communication, cryptographic APIs which contributes to a secure backend API.</li><li> **Con:**  Developers must stay vigilant about potential security vulnerabilities and keep dependencies up-to-date to benefit from the latest security patches.</li></ul> **Options Considered:** 
1.  **Other Programming Languages (e.g., Python, Node.js):**  Considered but not chosen due to specific requirements related to scalability, performance, and lack of possible expertise issue within the development team.

 | 
| Application will not need a dedicated mobile app  | Application access via web browser and no dedicated mobile app 
### Context
The Customer Management Platform System is designed to provide users with a comprehensive toolset for managing customer interactions, tracking leads, and facilitating communication. The primary user interface for the system will be delivered through web browsers. The decision to focus on web-based delivery has been made based on considerations related to user experience, development efficiency, and the absence of specific use cases requiring a dedicated mobile app.

 **Status:** Accepted


### Decision
Given the considerations outlined below, the decision is to proceed with the development of the Customer Management Platform System as a responsive web application, ensuring accessibility and usability on web browsers, including tablets. No dedicated mobile application will be developed at this time.


### Considerations

1.  **User Experience:** 

<ul><li>A responsive web application ensures a consistent user experience across various devices, including desktops, laptops, and tablets.</li></ul>
1.  **Development Efficiency:** 

<ul><li>Developing and maintaining a single codebase for a responsive web application is more efficient than managing separate codebases for web and mobile applications.</li></ul>
1.  **Target User Base:** 

<ul><li>The primary user base is expected to access the system from desktops and tablets. The absence of a dedicated mobile app aligns with the usage patterns and preferences of the target audience.</li></ul>
1.  **Cost Considerations:** 

<ul><li>Focusing on web-based development allows for cost-effective and streamlined development without the additional overhead of building and maintaining a separate mobile application.</li></ul>
1.  **Technological Considerations:** 

<ul><li>Modern web technologies and frameworks support responsive design, enabling the application to adapt to various screen sizes effectively.</li></ul>


### Rationale:

1.  **Consistent User Experience:** 

<ul><li>Users accessing the system through web browsers on different devices will experience a consistent and responsive interface.</li></ul>
1.  **Development Streamlining:** 

<ul><li>Development efforts will be focused on a single codebase, simplifying maintenance and updates.</li></ul>
1.  **Reduced Development Costs:** 

<ul><li>The decision avoids the additional costs associated with developing and maintaining a dedicated mobile application.</li></ul>


### Implications

1.  **Implementation Guidelines:** 

<ul><li>Develop and communicate guidelines for implementing responsive design principles throughout the development process.</li></ul>
1.  **Continuous Monitoring:** 

<ul><li>Establish a system for continuous monitoring of user analytics and feedback to assess the need for adjustments or future enhancements, including potential mobile app development.</li></ul>

 | 
| React.js as the framework for building the user interface | React.js as the framework for building the user interface
### Context
We are tasked with designing and implementing a Customer Management Platform (CMP) system. The system is expected to have a modern, responsive, and user-friendly front end. After evaluating various options, it has been decided to use React.js as the framework for building the user interface.

 **Status:** Accepted


### Decision
We have decided to build the front end of the CMP system using React.js. 


### Rationale:

1.  **Component-Based Architecture:**  React follows a component-based architecture, which allows us to break down the UI into reusable components. This modularity makes it easier to manage and maintain the codebase, especially as the CMP system may evolve over time with new features.


1.  **Virtual DOM for Efficient Rendering:**  React utilizes a virtual DOM, which improves rendering performance by minimizing actual DOM manipulations. This is crucial for a responsive user interface, especially in a CMP system where users interact with various data and views.


1.  **Rich Ecosystem and Community Support:**  React has a large and active community, providing a wealth of libraries, tools, and resources. This ecosystem facilitates faster development, easy integration with other technologies, and the availability of best practices.


1.  **Single Page Application (SPA) Support:**  React is well-suited for building Single Page Applications, where the user interacts with the application without the need for full page reloads. SPAs provide a smoother user experience, which is essential for a CMP system where users often navigate between different sections and data.




### Implications
While the decision to use React brings numerous benefits, there are some considerations and consequences:


1.  **Browser Compatibility:**  Although React is designed to work across different browsers, testing and ensuring compatibility with older browsers may be necessary.
1.  **Dependency Management:**  Regular updates to React and its ecosystem may require ongoing maintenance to keep the application up-to-date with the latest features and security patches.



 | 





Fitness Functions





|  **Performance Efficiency**  | 
1. User transaction should respond within the set limits  at peak load
    1. Read  <= 700ms (end to end) for 98 percentile transactions.
    1. Writes <=1.2 secs (end to end) for 98 percentile transactions.

    

 | 
1. Conduct Performance tests to optimally provision resources and optimise resource behaviour.
1. Implement data caching methodologies, data should be cached to edge locations  to enhance response time

 | 
1. Execute UAT and Pilot user testing.

 | 
|  **Availability**  | 
1. Platform components availability will be 99.95 %  end to end.
1. Upgrades should take place with minimal down time
    1. Upgrades to application as well as infrastructure should take place with zero down time.
    1. Upgrades to database should have < 30mins down time

    

 | 
1. Services are deployed across multiple regions.
    1. Services are loaded balanced across deployments

    
1. Provision automated failover
1. Utilize platform features related to self healing.
1. Utilize platform features related to rolling upgrades.
1. Automation of processes.

 | 
1. Execute testing and drills

 | 
|  **Scalability**  | 
1. System should be scalable to cater to sudden or projected growth in transactions 

 | 
1. Utilise container platforms capabilities.
    1. Configure auto scaling to progressively scale as required.
    1. Ability to serve request with minimal resource requirements.

    
1. Design stateless transactions.

 | 
1. Execute testing to validate all the use cases.

 | 
|  **Operational Excellence **  | 
1. Application should have minimal errors or deviation from requirements
1. Application should be resilient
1. RTO should be less than 5mins and RPO should be NIL
1. Intuitive, multi-channel and user-friendly interfaces.
    1. Simplified navigation and clear layouts

    

 | 
1. Create an elaborate list of use cases for testing ensuring all requirements are covered
1. Create a disaster recovery strategy
1. Provision data replication
1. Ensure proper cadence for backups
1. Ease of use of designed and developed UI
    1. User does not need help to understand UI

    

 | 
1. Conduct SIT testing to ensure that the application are adhering to the requirements
1. Conduct failover and disaster recovery activities
1. Carry out testing by end users to get their feedback and make iterative modifications.

 | 
|  **Security**  | 
1. Compliance with GDPR including consent management, PCIDSS.
1. Communication between components using HTTPs
1. Sensitive data should be encrypted at rest
1. Comprehensive authorisation and authentication mechanisms should be provisioned
1. Ensure RBAC, MFA and least privilege access.
1. Comprehensive logging and auditing of all customer data access and modifications.

 | 
1. Install certificates, utilise SSL/TLS protocols to exchange data.
1. Encryption of data at rest using cryptographic keys. 
    1. Safeguard cryptographic keys by storing using a secure solution e.g. Vault.

    
1. Personal Data and Sensitive Data attributes should be masked and stored in order to meet GDPR norms related to data privacy protection.
    1. Define data retention policies for sensitive customer and user data.

    
1. Assets should be accessed only by privileged users and after proper authentication.
    1. Grant access to users, groups, and applications at a specific scope. Use predefined roles. 

    
1. Services to be secured via Oauth
1. System users to be authenticated using Identity Provider.

 | 
1. Execute testing to validate all the use cases.

 | 



