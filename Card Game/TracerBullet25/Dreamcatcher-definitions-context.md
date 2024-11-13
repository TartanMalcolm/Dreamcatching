# DEFINITIONS FOR DREAMCATCHER

## 1. DREAMCATCHER PLATFORM
### Class Name:
DREAMCATCHER PLATFORM

### Description:
The DREAMCATCHER PLATFORM is a decentralized, AI-driven platform designed to address traditional startup limitations through incentive alignment, permissionless participation, and dynamic talent utilization. Bringing together a collaborative collection of NAPPs, it enables LEGAL ENTITIES to jointly develop, fund, and utilize NAPPs without requiring direct legal contracts. The platform’s decentralized governance model fosters innovation by transparently recording contributions, distributing rewards based on actual inputs, and creating an inclusive environment where global talent can freely contribute and be recognized.

### Attributes:
A collection of NAPPs managed and utilized within the platform.

### Provides:
CONTRIBUTION: Records all activities and events by USERS within the platform.
ATTRIBUTION: Distributes value among CONTRIBUTORS based on their recorded contributions.
STUCK LOOP: Mechanisms to identify and resolve situations where progress is halted.
USER Interface: Interfaces that allow USERS to interact with NAPPs and the platform.

### Consumes:
GATEWAY-SERVICES: Services provided by GATEWAYs to handle interactions with the legal world and ensure compliance.

### Associations:
USERS: Enables USERS (such as FUNDERS, TALENT, CONSUMERS, TRADERS) to participate in developing, funding, utilizing, and trading NAPPs.
GATEWAYs: Relies on GATEWAYs to bridge interactions with the legal world, ensuring compliance and handling contracts on behalf of USERS.
CONTRIBUTION: Utilizes the CONTRIBUTION ledger to record user activities.
ATTRIBUTION: Uses the ATTRIBUTION system to distribute value based on contributions.
DREAMCATCHER FOUNDATION: Utilizes frameworks, standards, and protocols provided to maintain interoperability and governance.

### Generalizations (Inheritance):
None.

### Interactions:
With USERS: Facilitates participation in the ecosystem without the need for direct legal contracts.
With GATEWAYs: Relies on GATEWAYs for legal compliance and contract handling.
Between USERS: Enables indirect collaboration and value exchange through the CONTRIBUTION ledger and ATTRIBUTION mechanism.
With DREAMCATCHER FOUNDATION: Aligns with provided frameworks and standards to ensure interoperability and effective governance.

## 2. GATEWAYs
### Class Name:
GATEWAY

### Description:
GATEWAYs serve as intermediaries within the DREAMCATCHER PLATFORM, facilitating legal compliance, contract handling, and regulatory interactions for USERS. They streamline complex legal requirements by managing AML and KYC processes, liability, and dispute resolution, enabling USERS to focus on core activities without legal barriers. By supporting INTER-GATEWAY AGREEMENTS, GATEWAYs also enable global collaboration, ensuring seamless and compliant cross-jurisdictional interactions.

### Attributes:
A range of GATEWAY-SERVICES offered to LEGAL ENTITIES.
Compliance mechanisms, including AML (Anti-Money Laundering) and KYC (Know Your Customer) procedures.
Support for Decentralized Identity (DID), allowing USERS to control their identity without relying on centralized providers.

### Provides:
GATEWAY-SERVICES: Services to LEGAL ENTITIES for consuming third-party services.
LEGAL COMPLIANCE: Ensures that all interactions comply with relevant laws and regulations.
Management of liabilities and responsibilities between LEGAL ENTITIES and other GATEWAYs.
TRADING-AS arrangements, facilitating USERS operating under trading names.
Dispute resolution mechanisms.

### Consumes:
Licenses, software, and protocols from the DREAMCATCHER FOUNDATION.
INTER-GATEWAY AGREEMENTS with other GATEWAYs to enable interoperability.

### Associations:
USERS: Enters into individual contracts, providing services and compliance mechanisms for participation.
CONSUMERS: Acts as the legal contracting party, handling transactions on behalf of USERS operating under TRADING-AS names.
GATEWAY-SERVICES: Offers additional services by contracting with third-party providers.
Other GATEWAYs: Collaborates through INTER-GATEWAY AGREEMENTS.
DREAMCATCHER FOUNDATION: Receives necessary licenses and protocols to operate.

### Generalizations (Inheritance):
None.

### Interactions:
With USERS: Provides necessary services for participation, ensuring legal compliance.
With CONSUMERS: Facilitates transactions and handles contracts on behalf of USERS.
Among GATEWAYs: Works with others to enable cross-jurisdictional activities and interoperability.
With DREAMCATCHER FOUNDATION: Aligns with standards and obtains required licenses.

## 3. USERS
### Class Name:
USER

### Description:
USERS are LEGAL ENTITIES who join the DREAMCATCHER PLATFORM to participate in roles such as FUNDER, TALENT, CONSUMER, or TRADER. Through this role flexibility, USERS contribute according to their interests and strengths, with the platform’s CONTRIBUTION ledger ensuring all activities are transparently recorded. This approach allows USERS to be fairly compensated for their contributions, aligning individual success with the platform’s overall progress.

### Attributes:
A unique identifier for the USER.
The roles currently assumed (e.g., FUNDER, TALENT).

### Provides:
Varies based on the role assumed; see specific roles for details.

### Consumes:
Varies based on the role assumed; see specific roles for details.

### Associations:
LEGAL ENTITY: Each USER is a LEGAL ENTITY that contracts with a GATEWAY.
Roles: Associates with specific roles, inheriting attributes and behaviors from those roles.

### Generalizations (Inheritance):
Inherits from: LEGAL ENTITY
Specializes into: FUNDER, TALENT, CONSUMER, TRADER

### Interactions:
See specific roles for detailed interactions.

## 4. FUNDERS
### Class Name:
FUNDER

### Description:
FUNDERS are USERS who provide financial resources within the DREAMCATCHER PLATFORM to support NAPP development. They encourage innovation by offering bounties for specific projects or initiatives, which are recorded as CONTRIBUTIONS. Through the ATTRIBUTION system, FUNDERS can participate in value distribution, ensuring their financial contributions are recognized in proportion to the impact they enable.

### Attributes:
The total amount of financial resources offered.
A list of bounties posted for projects and initiatives.

### Provides:
Offers bounties for projects and initiatives, which are recorded as CONTRIBUTIONS.

### Consumes:
ATTRIBUTION: Receives potential returns based on contributions.
GATEWAY-SERVICES: Utilizes transaction management services provided by GATEWAYs.

### Associations:
CONTRIBUTION: Financial contributions are recorded as bounties.
ATTRIBUTION: Engages in value distribution, receiving returns based on contributions.
GATEWAY-SERVICES: Relies on services for transaction management and legal compliance.
TALENT: Indirectly supports TALENT by funding their projects.

### Generalizations (Inheritance):
Inherits from: USER

### Interactions:
With TALENT: Supports projects by offering bounties, enabling TALENT to contribute.
With GATEWAYs: Manages funding transactions and ensures legal compliance.
With ATTRIBUTION: Participates in value distribution based on contributions.
With the DREAMCATCHER PLATFORM: Engages to offer bounties and support development.

## 5. TALENT
### Class Name:
TALENT

### Description:
TALENT are USERS who contribute skills, labor, or intellectual property to enhance NAPPs within the DREAMCATCHER PLATFORM. Through their collaboration and problem-solving efforts, TALENT drives the platform's innovation and growth. The CONTRIBUTION ledger transparently records their work, while the ATTRIBUTION system ensures they receive fair compensation based on their measurable contributions, enhancing motivation and professional satisfaction.

### Attributes:
Specific skills or areas of expertise brought to projects.
Work, ideas, or intellectual property contributed to NAPP development.

### Provides:
Expertise and work toward creating or improving NAPPs.
Skill-based contributions recorded in the platform's ledger.

### Consumes:
ATTRIBUTION: Receives value and compensation reflecting contributions.
GATEWAY-SERVICES: Utilizes services for compliance and support.
Funding from FUNDERS to support their work.
Tips from TRADERS as additional compensation.

### Associations:
CONTRIBUTION: Records their work and activities.
ATTRIBUTION: Distributes value based on contributions.
GATEWAY-SERVICES: Provides compliance mechanisms and support services.
FUNDERS: Receives funding for projects.
TRADERS: May accept or reject offers and tips.
Other TALENT: Collaborates with others to enhance NAPPs.

### Generalizations (Inheritance):
Inherits from: USER

### Interactions:
With FUNDERS: Receives funding to support development.
With other TALENT: Collaborates to solve problems and enhance NAPPs.
With GATEWAYs: Uses services for participation and compliance.
With TRADERS: May accept or reject offers for contributions.
With NAPPs: Contributes to development and improvement.

## 6. CONSUMERS
### Class Name:
CONSUMER

### Description:
CONSUMERS are USERS who utilize the NAPPs developed within the DREAMCATCHER PLATFORM, actively contributing to the ecosystem through their usage and feedback. Their interactions with NAPPs are recorded in the CONTRIBUTION ledger, allowing CONSUMERS to shape ongoing development and improvement based on real-world use, supporting a responsive and user-centered innovation process.

### Attributes:
A record of NAPPs used.
Feedback provided to developers.

### Provides:
Usage data and feedback, influencing development.
Support to the ecosystem through utilization.

### Consumes:
NAPPs: Utilizes applications developed on the platform.
GATEWAY-SERVICES: Receives legal protection and compliance services.

### Associations:
NAPPs: Uses and interacts with applications.
GATEWAY-SERVICES: Engages in transactions and agreements for compliance.
TALENT: Indirectly supports developers through usage and feedback.

### Generalizations (Inheritance):
Inherits from: USER

### Interactions:
With NAPPs: Utilizes applications and provides feedback.
With GATEWAYs: Ensures compliance during usage.
With TALENT: Influences development through feedback and usage patterns.

## 7. TRADERS
### Class Name:
TRADER

### Description:
TRADERS are USERS who offer payments to CONTRIBUTORS after a NAPP is available for use, allowing for additional compensation directly linked to a NAPP's real-world impact. Payments accepted by CONTRIBUTORS are recorded as new CONTRIBUTIONS and reflected in the ATTRIBUTION system, promoting a flexible and market-responsive value distribution model within the DREAMCATCHER PLATFORM.

### Attributes:
A list of payments or offers made to CONTRIBUTORS.

### Provides:
Additional compensation to CONTRIBUTORS, influencing value distribution.

### Consumes:
GATEWAY-SERVICES: Utilizes transaction facilitation services.

### Associations:
CONTRIBUTION: Accepted payments result in new contributions being recorded.
GATEWAY-SERVICES: Ensures compliance during transactions.
CONTRIBUTORS: Interacts with TALENT and others to offer payments.

### Generalizations (Inheritance):
Inherits from: USER

### Interactions:
With CONTRIBUTORS: Offers direct payments or rewards.
With GATEWAYs: Ensures legal compliance during transactions.
With DREAMCATCHER PLATFORM: Influences value distribution by rewarding specific contributions.

## 8. CONTRIBUTION
### Class Name:
CONTRIBUTION

### Description:
CONTRIBUTION serves as an immutable record within the DREAMCATCHER PLATFORM, logging all actions and contributions by USERS. This record is foundational to the platform’s incentive model, providing transparent data for the ATTRIBUTION system to assign value and distribute rewards equitably among CONTRIBUTORS. The CONTRIBUTION ledger builds trust within the ecosystem, supporting fair recognition of individual efforts.

### Attributes:
Logs of all actions and contributions made by USERS.
Unique identifiers for each contribution.
Types of contributions (e.g., financial, skill-based).
Timestamps of when contributions were made.

### Provides:
Transparent activity logs.
Foundational data for the ATTRIBUTION system.

### Consumes:
GATEWAY-SERVICES: For ledger maintenance and ensuring compliance.

### Associations:
USERS: Records their activities and contributions.
ATTRIBUTION: Used to calculate value distribution.
GATEWAYs: Referenced for compliance and validation purposes.

### Generalizations (Inheritance):
None.

### Interactions:
With USERS: Logs actions, impacting rewards and recognition.
With ATTRIBUTION: Provides the data needed to distribute value fairly.
With GATEWAYs: Used for compliance checks and validation.

## 9. ATTRIBUTION
### Class Name:
ATTRIBUTION

### Description:
ATTRIBUTION is a core system within the DREAMCATCHER PLATFORM that interprets data from the CONTRIBUTION ledger to assign value and distribute rewards to CONTRIBUTORS during DISPERSAL EVENTS. This transparent and objective mechanism aligns incentives with actual contributions, ensuring fair compensation based on measurable impact, promoting trust and motivation across the ecosystem.

### Attributes:
Algorithms used to calculate value distribution.
History of dispersals and value distributions.

### Provides:
Fair compensation reflecting the actual input of each CONTRIBUTOR.
Transparent operation with agreed-upon rules.

### Consumes:
CONTRIBUTION data: Uses the recorded contributions to calculate distributions.
GATEWAY-SERVICES: Coordinates financial transactions and ensures compliance.

### Associations:
CONTRIBUTORS: Distributes rewards based on contributions.
GATEWAYs: Works with them to facilitate transactions and ensure compliance.

### Generalizations (Inheritance):
None.

### Interactions:
With CONTRIBUTORS: Determines and distributes rewards.
With GATEWAYs: Coordinates transactions and ensures legal compliance.

## 10. TRADING-AS
### Class Name:
TRADING-AS

### Description:
TRADING-AS allows a USER or group of USERS to operate under a trading name different from their legal or personal names. Supported by GATEWAYs, this feature facilitates branding, enabling collaboration without forming a new legal entity, and promotes professional engagement within the DREAMCATCHER PLATFORM.

### Attributes:
The trading name under which the USER or group operates.
USERS associated with this trading name.

### Provides:
Branding and marketing under a unified name.
Ability for collaborative operation without forming new entities.

### Consumes:
GATEWAY-SERVICES: For management and legal facilitation.
Verification services to prevent trademark issues.

### Associations:
GATEWAYs: Establishes agreements for legal use of trading names.
CONSUMERS: Offers products or services under the trading name.
Other USERS: Collaborates under a shared identity.

### Generalizations (Inheritance):
None.

### Interactions:
With GATEWAYs: Sets up legal arrangements for trading names.
With CONSUMERS: Operates under the trading name in the marketplace.
With Other USERS: Enables collaboration under a unified brand.

## 11. LEGAL ENTITIES
### Class Name:
LEGAL ENTITY

### Description:
LEGAL ENTITIES are individuals, companies, organizations, or incorporated bodies that contract with GATEWAYs to interact within the DREAMCATCHER PLATFORM. LEGAL ENTITIES participate through roles like USERS, enabling participation while maintaining compliance with platform-wide standards set by the DREAMCATCHER FOUNDATION.

### Attributes:
A unique identifier for the legal entity.
Official registered name.
Contracts and agreements entered with GATEWAYs.

### Provides:
Legal capacity to enter contracts and hold rights.
A formal structure for managing liabilities.

### Consumes:
GATEWAY-SERVICES: For participation and compliance.
NAPPs: For development or utilization.

### Associations:
GATEWAYs: Enters agreements to access services.
USERS: Can act as USERS by participating in roles.
DREAMCATCHER FOUNDATION: Operates within established frameworks and standards.

### Generalizations (Inheritance):
Superclass for USER

### Interactions:
With GATEWAYs: Contracts for access and services.
With Other LEGAL ENTITIES: Collaborates or transacts within the ecosystem.
With DREAMCATCHER FOUNDATION: Aligns operations with provided standards.

## 12. GATEWAY Network
### Class Name:
GATEWAY NETWORK

### Description:
The GATEWAY NETWORK is a collective of GATEWAYs in different jurisdictions, collaborating to provide unified, compliant access to LEGAL ENTITIES globally. It ensures that USERS have consistent services and standards across jurisdictions through INTER-GATEWAY AGREEMENTS, facilitating global interaction and innovation.

### Attributes:
A list of GATEWAYs that are part of the network.
Standards and protocols followed within the network.

### Provides:
Global compliance and participation.
Consistent services and standards across jurisdictions.

### Consumes:
INTER-GATEWAY AGREEMENTS to enable interoperability and compliance.
Local regulations and requirements for each jurisdiction.

### Associations:
GATEWAYs: Comprises multiple GATEWAYs.
LEGAL ENTITIES: Provides seamless access regardless of location.
DREAMCATCHER FOUNDATION: Aligns with provided standards and protocols.

### Generalizations (Inheritance):
None.

### Interactions:
Among GATEWAYs: Collaborates on compliance and services.
With LEGAL ENTITIES: Facilitates access and interactions globally.
With DREAMCATCHER FOUNDATION: Aligns with frameworks and standards.

## 13. DREAMCATCHER FOUNDATION
### Class Name:
DREAMCATCHER FOUNDATION

### Description:
The DREAMCATCHER FOUNDATION is the central organization providing frameworks, standards, and guidelines that govern interactions across GATEWAYs within the DREAMCATCHER PLATFORM. By establishing open-source protocols and interoperability standards, it ensures that LEGAL ENTITIES can participate securely and effectively, creating a foundation for decentralized, compliant collaboration.

### Attributes:
A set of standards and protocols provided.
Types of licenses available.
Specifications for NAPPs.

### Provides:
Licenses, software, and protocols necessary for platform operation.
Standards for interoperability and governance.
NAPP-FORMAT specifications to ensure consistency.

### Consumes:
Feedback and contributions from the community.
Open-source developments.

### Associations:
GATEWAYs: Supplies necessary tools and standards.
NAPPs: Provides format specifications for development.
LEGAL ENTITIES: Sets frameworks within which they operate.

### Generalizations (Inheritance):
None.

### Interactions:
With GATEWAYs: Provides licenses, protocols, and standards.
With NAPP Developers: Supplies specifications and supports development.

## 14. INTER-GATEWAY AGREEMENTS
### Class Name:
INTER-GATEWAY AGREEMENT

### Description:
INTER-GATEWAY AGREEMENTS establish interoperability and compliance standards between GATEWAYs, allowing LEGAL ENTITIES across jurisdictions to interact seamlessly. These agreements support standardized operations and cross-jurisdictional collaboration, promoting a unified experience within the DREAMCATCHER PLATFORM.

### Attributes:
Unique identifiers for the agreements.
Terms and conditions agreed upon.

### Provides:
Standardized operations across GATEWAYs.
Cross-jurisdictional support for LEGAL ENTITIES.

### Consumes:
Mutual responsibilities and standards defined in the agreement.
Procedural alignments to ensure smooth collaboration.

### Associations:
GATEWAYs: Agreements are made between them.
USERS: Facilitates seamless operation across different GATEWAYs.

### Generalizations (Inheritance):
None.

### Interactions:
Among GATEWAYs: Enables unified services and experiences.
With LEGAL ENTITIES: Provides consistent access and operations.

## 15. GATEWAY-SERVICES
### Class Name:
GATEWAY-SERVICES

### Description:
GATEWAY-SERVICES encompass the suite of services provided by GATEWAYs to LEGAL ENTITIES, including compliance, identity management, and transaction processing. They allow LEGAL ENTITIES to securely participate in the DREAMCATCHER PLATFORM and facilitate seamless access to third-party integrations, enhancing the platform’s functionality.

### Attributes:
A list of available services.
Integrations with external service providers.

### Provides:
Compliance services (e.g., KYC, AML).
TRADING-AS arrangements.
Billing, payment processing, and reporting.
Access to third-party service providers, Large Language Models (LLMs), and APIs.

### Consumes:
Services from external providers.
Standards and protocols from the DREAMCATCHER FOUNDATION.

### Associations:
LEGAL ENTITIES: Enables participation by providing essential services.
Third-Party Providers: Integrates functionalities to enhance the user experience.
DREAMCATCHER FOUNDATION: Adheres to provided standards and infrastructure.

### Generalizations (Inheritance):
None.

### Interactions:
With LEGAL ENTITIES: Facilitates access to necessary services.
With Third-Party Providers: Integrates services to enhance functionality.
With DREAMCATCHER PLATFORM: Supports the platform's operations.

## 16. NAPPs (Natural Language Applications)
### Class Name:
NAPP

### Description:
NAPPs are modular, reusable software components designed for interoperability within the DREAMCATCHER PLATFORM. They can integrate AI-based natural language processing and be dynamically composed with other NAPPs into Just in Time Applications (JITAs), allowing for agile, on-demand functionality that adapts to USER interactions and needs.

### Attributes:
Unique identifiers for each NAPP.
Components such as AGENTS, TOOLS, GRAPHICS, EFFECTS.
Format specifications based on JSON.
Natural language system prompts for AI integration.
Dependencies on other NAPPs.
Specified runtime environments.

### Provides:
Functionalities for use, extension, or integration.
Components that can be combined into JITAs.

### Consumes:
RUNTIME environments as specified.
GATEWAY-SERVICES for management and distribution.

### Associations:
USERS: Developed by TALENT, funded by FUNDERS, used by CONSUMERS, traded by TRADERS.
Other NAPPs: Can depend on or integrate with them.
GATEWAY-SERVICES: Managed and distributed through these services.
DREAMCATCHER FOUNDATION: Adheres to provided format specifications.

### Generalizations (Inheritance):
None.

### Interactions:
With USERS: Central to development, funding, use, and trading activities.
With Other NAPPs: Can be composed into larger applications.
With DREAMCATCHER FOUNDATION: Aligns with provided specifications and standards.

## 17. JITA (Just in Time Applications)
### Class Name:
JITA

### Description:
JITAs dynamically combine NAPPs to form customized applications based on USER interactions. This model of application generation enables responsive, personalized functionality, adapting the platform’s capabilities to specific needs in real-time while maintaining interoperability within the DREAMCATCHER PLATFORM.

### Attributes:
Unique identifiers for each JITA.
The NAPPs involved in the composition.

### Provides:
Functionalities based on the conversation thread between the USER and a NAPP.
May combine visual display items and interactive elements.

### Consumes:
RUNTIME environments as specified.
GATEWAY-SERVICES for compliance and management.

### Associations:
USERS: Provides the primary interface for interaction.
NAPPs: Combines various NAPPs to deliver functionality.
GATEWAY-SERVICES: Ensures compliance and proper operation.

### Generalizations (Inheritance):
None.

### Interactions:
With USERS: Serves as the interface for NAPPs, enabling personalized interaction.
With NAPPs: Combines multiple NAPPs to deliver tailored functionality.
With GATEWAY-SERVICES: Managed and distributed appropriately, ensuring legal compliance.
