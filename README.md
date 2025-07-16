## Project Overview

The **Salesforce Tours & Travels Customer Relationship Management (CRM) Platform** is a tailored solution designed to optimize the core operations of travel and tour businesses by leveraging Salesforce’s robust CRM capabilities. This platform centralizes the management of client inquiries, travel package selections, bookings, payments, and post-travel feedback, providing a seamless and unified experience for both staff and customers.

By automating essential tasks such as booking approvals, customer notifications, and follow-up reminders using tools like **Flows** and **Process Builder**, the system significantly enhances operational efficiency and accuracy. It also elevates the customer experience through personalized communication and secure handling of sensitive information.

Moreover, the platform delivers real-time insights through **dynamic reports and interactive dashboards**, empowering travel agencies to make informed, data-driven decisions. Ultimately, this project offers a reliable, scalable CRM solution that enables agencies to streamline workflows, improve service quality, and support sustainable business growth.

## Documentations Links and References
<img src="https://img.favpng.com/2/8/11/package-tour-travel-agent-icon-png-favpng-qKtDRnC16sTUrjpLtTKUWgbBx.jpg" alt="Travel Icon" width="250"/>

## Tours and Travel Salesforce Documentation [Click here to view the full documentation](https://docs.google.com/document/d/1cALV3hFovfY-NoTzyRLODfsDWJ4vMqaomgWrMK_uwos/edit?usp=sharing)

# Phase 1: Requirements Analysis & Planning 
This phase focused on understanding the travel industry’s core business needs and translating them into a scalable Salesforce CRM solution. Key activities included gathering user requirements, defining project scope, and creating a technical roadmap to guide development. I designed the data and security models to reflect real-world travel workflows, supporting features such as booking management, customer tracking, and secure access control. This early planning ensured that the system would be structured, scalable, and aligned with both user expectations and long-term business goals.

## Understanding Business Requirements
The first milestone focused on uncovering key operational challenges faced by travel agencies, such as manual booking workflows, slow customer communication, lack of centralized feedback management, and limited cross-team coordination. By evaluating the needs of primary stakeholders—including travel agents, finance staff, and customers I translated these issues into concrete CRM requirements like booking automation, unified customer records, and real-time alerts. 

This phase deepened my understanding of how to bridge business problems with technical solutions. It also enhanced my ability to perform stakeholder analysis, prioritize user needs, and design a CRM system that addresses fragmented processes using Salesforce as an integrated platform.

## Defining Project Scope & Objectives
This milestone focused on clearly defining the scope and objectives of the CRM system. The platform was designed to manage the entire travel process from initial booking inquiries to post-trip feedback while remaining scalable for global use. Key functional needs included support for group travel, tiered memberships, dynamic pricing, and secure role-based data access. The overall goals were centered on streamlining operations through automation, improving communication speed, and enabling actionable insights through analytics.

Working through this phase strengthened my ability to set clear system boundaries. I learned the value of explicitly defining what the CRM should and shouldn’t include—especially within a limited development timeframe. This clarity helped shape development priorities and ensured that focus remained on delivering the most critical features first.


## Gathering & Analyzing User Needs

This milestone focused on understanding the unique expectations and workflows of various CRM user groups, including travel agents, customers, tour guides, finance personnel, and administrators. To simulate real-world interactions, I created user personas and mapped out journey flows using tools like Miro boards and feedback forms. From these insights, I identified essential features such as group travel management, dynamic pricing, automated follow-ups, and multilingual support.

Through this process, I learned the importance of putting user experience at the center of design. By walking through user journeys and identifying pain points, I was able to prioritize features that deliver meaningful value to each stakeholder. This phase reinforced how empathy-driven planning leads to more intuitive and effective system design.



## Identifying Salesforce Tools & Features

With the user and business requirements defined, I selected the appropriate Salesforce components to implement the desired functionality. Custom objects such as `Booking`, `TravelPackage`, and `Feedback` were planned to capture key data. To automate processes, I mapped requirements to tools like **Flows**, **Process Builder**, and **Approval Processes**. For advanced logic, features such as **Apex Triggers**, **Batch Apex**, and **Lightning Web Components (LWC)** were included. Security controls were planned using **Profiles**, **Permission Sets**, and **Sharing Rules**.

This step helped me understand how to match the right Salesforce tools to each business goal. It also taught me how to balance declarative solutions with code-based customization for optimal flexibility and long-term maintainability.



## Designing the Data Model & Security Architecture

In this milestone, I developed a relational data model to reflect how records connect across the CRM. Core relationships linked `Booking` with `Customer_Info`, `TravelPackage`, and `Employee` (as assigned guides). Supporting objects like `BookingGuest` and `Feedback` captured group details and post-travel insights. The security structure was built using a clear role hierarchy (e.g., Manager > Agent > Guide), field-level protections (e.g., finance-related fields hidden from agents), and record-level access managed through sharing settings.

This part of the project taught me how to design for both usability and data protection. I developed a stronger understanding of how Salesforce handles object relationships, access control, and compliance. Ensuring the right users have access to the right data, without sacrificing performance or security, was a key takeaway from this phase.

# Phase 2: Salesforce Development - Backend & Configuration

This phase focused on building the backend architecture of the Tours & Travels CRM using a combination of Salesforce's declarative tools and programmatic features. The objective was to define custom data models, apply validation rules, and automate critical processes like booking and payment workflows. Tools such as **Flows**, **Process Builder**, and **Apex** were used to ensure the system operates efficiently and scales with business growth. A total of **12 technical milestones** were completed, each contributing to a reliable, secure, and maintainable backend infrastructure.

## Milestone 1: Setting Up the Salesforce Developer Org

To kick off my Salesforce journey, I created a Salesforce Developer Org to serve as the foundation for hands-on practice and project development. I started by registering at [developer.salesforce.com/signup](https://developer.salesforce.com/signup), where I filled in the required fields—using "Developer" for both job title and company name. After submitting the form, I received a verification email, which I confirmed to activate the account. I then set up my password and successfully logged in via [login.salesforce.com](https://login.salesforce.com). With this setup complete, my dedicated Salesforce Developer environment was ready for building and testing CRM solutions.

![Milestone 1 - Salesforce Account](./ScreenshotDocumentation/Milestone1SalesforceAccount.PNG)

## Milestone 2: Object Creation

To establish the core data structure for the **Tours & Travels CRM**, seven custom objects were created to represent key business entities:

- `Customer_Info__c`  
- `Booking__c`  
- `BookingGuest__c`  
- `TravelPackage__c`  
- `BookingPayment__c`  
- `Employee__c`  
- `Feedback__c`

Each object was designed with primary fields and **lookup relationships** to accurately reflect real-world business logic. For instance, the `Booking__c` object is linked to both the `Customer_Info__c` and `TravelPackage__c` objects, establishing crucial connections between customers, bookings, and tour packages.

This milestone strengthened my understanding of Salesforce’s **object-oriented architecture**. I learned that custom objects go beyond data storage—they define:
- Data relationships between entities  
- Automation logic (e.g., triggers and flows)  
- User interface elements and behavior  
By setting up these custom objects correctly, I laid a strong foundation for scalable development and CRM automation in later phases.

![Milestone 2 - Object Creation](./ScreenshotDocumentation/Milestone2ObjectsCreation.PNG)

## Milestone 3: Tabs Creation

To enhance accessibility and navigation within the Salesforce interface, I created **custom tabs** for each of the core objects in the **Tours & Travels CRM** system.

### Steps Taken:
1. Navigated to `Setup`.
2. Searched for **"Tabs"** using the Quick Find box.
3. Selected the **Tabs** section under **User Interface**.
4. Under **Custom Object Tabs**, clicked **New** to begin the process.

For each tab:
- Selected the relevant custom object (e.g., `Customer_Info__c`).
- Chose a tab icon and color for visual representation.
- Kept default visibility settings for user profiles.
- Opted **not** to include the tab in apps by default but allowed it to appear in users' personal customizations.
- Clicked **Save** to finalize creation.

### Tabs Created for the Following Custom Objects:
- `Customer_Info__c`
- `Booking__c`
- `BookingGuest__c`
- `TravelPackage__c`
- `BookingPayment__c`
- `Employee__c`
- `Feedback__c`
![Milestone 3 - Tabs Creation](./ScreenshotDocumentation/Milestone3TabCreation.PNG)

## Milestone 4: Fields & Relationships
In this milestone, I focused on designing and implementing all essential fields and object relationships for the Tours & Travels CRM system. On the `Customer_Info__c` object, key fields such as `Email` were created using appropriate data types and configured to support search and reporting functionalities. A global picklist value set for `Country` was also defined and reused across various objects to maintain consistency and scalability.

To maintain relational integrity, a lookup relationship was established from the `Booking__c` object to `Customer_Info__c`, ensuring that every booking could be directly associated with a customer. In addition, a formula field was created on the `BookingGuest__c` object to dynamically calculate and categorize guest age groups, improving personalization and segmentation.

Picklist fields such as `Relation with Customer`, `Availability Status`, and `Payment Method` were added to capture critical business data. Multi-select picklists for fields like `Membership`, `Package Type`, and `Transportation Modes` enabled greater flexibility when defining travel offerings. For employee-related configurations, I added picklists for roles, departments, supported languages, and assigned regions. Location-specific fields like `Country` and `City` were tied to the global value sets, ensuring data consistency across all entries.

All field types were thoughtfully selected to support both user input and system automation. This setup ensures accurate data collection, real-world workflow alignment, and a strong foundation for reporting, automation, and future enhancements in the CRM.

![123](./ScreenshotDocumentation/Milestone4Fields&Relationships1.PNG)
![123](./ScreenshotDocumentation/Milestone4Fields&Relationships2.PNG)
![123](./ScreenshotDocumentation/Milestone4Fields&Relationships3.PNG)

## Milestone 5: Field Dependencies
To improve data accuracy and streamline user input across the CRM, I configured field dependencies between related picklist fields on key custom objects. On the `BookingGuest__c` object, a dependency was created between the `Country` and `City` fields. When a user selects a country, only cities relevant to that country become selectable, minimizing input errors and enhancing user experience.

On the `Booking__c` object, I implemented a dependency between `Membership` and `Preferred Accommodation`. Depending on the membership tier selected (e.g., Basic, Gold, or VIP), the system dynamically filters accommodation choices such as hotels, resorts, or villas. This ensures that booking options remain aligned with customer entitlements and business rules.

For the `Employee__c` object, I linked the `Department` field with the `Role` field, so that only appropriate roles—like Travel Agent, Finance Executive, or Tour Coordinator—appear under relevant departments such as Travel Operations, Finance, or Logistics. These dependencies help enforce logical consistency, reduce invalid entries, and simplify the user interface for data entry across the platform.
![123](./ScreenshotDocumentation/Milestone5FieldDependencies.PNG)

## Milestone 6: Validation Rules 

To uphold data integrity and enforce business-specific rules across the Tours and Travels CRM, I implemented several validation rules on key custom objects. On the `Customer_Info__c` object, validations were added to ensure that phone numbers contain exactly 10 digits, email addresses follow the correct format, and birthdates cannot be set in the future. For the `BookingGuest__c` object, the system enforces that age values must be greater than zero, and email addresses are required based on the assigned guest role.

On the `Employee__c` object, validation logic ensures that employees designated as guides must have at least one language selected, supporting complete and accurate role configuration. Additionally, the `Booking__c` object includes a rule that mandates all newly created booking records to default to a "Pending" status. These validation rules collectively reduce the risk of incorrect data entry and help maintain consistency and reliability across all records in the CRM.
![123](./ScreenshotDocumentation/Milestone6ValidationRules.PNG)




















