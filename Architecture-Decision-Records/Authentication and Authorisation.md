# User Onboarding and Authentication Strategy
## Context
The need for a robust User Onboarding and Authentication Strategy has been identified for our system. User authentication is a critical aspect of the application, and a combination of Azure AD tokens and Okta is proposed to address the requirements.
## Status
Accepted
## Decision
The decision is to employ Azure AD tokens for user authentication and Okta for machine-to-machine (M2M) authentication.
## Rationale
### 1. Azure AD Token for User Authentication:
1. Azure AD is a widely-used identity and access management service that provides secure and seamless user authentication.
2. Leveraging Azure AD tokens ensures compliance with industry standards and best practices for user authentication.
3. Azure AD supports a variety of authentication methods, including multi-factor authentication (MFA), enhancing the overall security posture of the application.
### 2. Okta for Machine-to-Machine (M2M) Authentication:
1. Okta is well-suited for M2M authentication, providing a scalable and secure solution for interactions between machines or services.
2. Okta offers robust APIs and integration capabilities, allowing for seamless integration with various machine-driven processes within the system.
3. This separation of user and machine authentication helps manage access controls more effectively and enhances the overall security of the system.
## Alternatives Considered
### 1. Using Azure AD for Both User and Machine Authentication:
While Azure AD supports M2M authentication scenarios, introducing Okta for this purpose provides a specialized solution tailored for machine-driven processes.
Okta's specific focus on M2M interactions may lead to better performance and scalability in scenarios involving numerous machine- authenticated requests.
### 2. Choosing an Alternative M2M Authentication Provider:
Considered other identity providers for M2M authentication, but Okta was selected based on its reputation, feature set, and proven track record in not just airline but also with financial institutions like S&P , Nasdaq.
## Implications
### 1. Integration Effort:
Development teams need to integrate both Azure AD and Okta into the system. Proper documentation and support will be essential to
facilitate a smooth integration process.
### 2. Maintenance and Support:
Teams responsible for maintaining the authentication components should be familiar with both Azure AD and Okta, necessitating
appropriate training and documentation. 
### 3. Cost Considerations:
Evaluate the cost implications of using both Azure AD and Okta. While Azure AD may be part of existing subscriptions, Okta's cost
should be factored into the overall budget. 
### 4. Security Monitoring:
Implement a comprehensive security monitoring solution to track user and machine authentication events, ensuring timely detection of any suspicious activities.
