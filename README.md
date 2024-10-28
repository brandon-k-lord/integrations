# integrations

## Table of Contents

- [integrations](#integrations)
  - [Table of Contents](#table-of-contents)
  - [Third-Party Integrations](#third-party-integrations)
    - [AI Assistance](#ai-assistance)
    - [Authentication Software](#authentication-software)
    - [Banking Core](#banking-core)
    - [Business Process Decision Modeling (BPM)](#business-process-decision-modeling-bpm)
    - [Document Compliance Solution](#document-compliance-solution)
    - [Financial Statement OCR](#financial-statement-ocr)
    - [Industry Market Research](#industry-market-research)

## Third-Party Integrations

**Background**:\
The competitive landscape in product development requires the skillset to identify when products need to be built and when products need to be integrated. Great strategy delivers success.

**Summary**:\
Section briefly discusses integrations initiatives. Discussion points focus on integration experience.

| Initiatives                                                   | Description                                                                                                                                      |
| ------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| [AI Assistance](#ai-assistance)                               | Artificial Intelligence assistance for producing financial narratives.                                                                           |
| [Authentication Software](#authentication-software)           | Authentication and authorization for user role definition and self-sign-up.                                                                      |
| [Banking Core](#banking-core)                                 | Back-end system connecting multiple branches of a financial institution for account opening, deposists, checking, savings, loan processing, etc. |
| [Business Process Modelors](#banking-core)                    | Back-end system connecting multiple branches of a financial institution.                                                                         |
| [Document Compliance Solution](#document-compliance-solution) | Compliance engine for generating loan documents.                                                                                                 |
| [Financial Statement OCR](#financial-statement-ocr)           | Extracting data from financial statements, automating data entry.                                                                                |
| [Industry Market Research](#industry-market-research)         | Statistical data for regulatory compliant industry analyses to identify external factors in the underwriting process.                            |

### AI Assistance

AI (Artificial Intelligence) is a powerful tool that can be leveraged to provide great customer value.

**Problem**:\
Credit analysis requires a narrative to explain the financial trends and ratios. With a basic template to fill in percentage change and financial ratios, these narratives can average 30 mins.

**Solution**:\
AI solution could ingest the financial data and produce a robust narrative with 10x the depth in seconds. A session was triggered during than credit analysis workflow and allowed for a conversation to take place with the user. The conversation would enable the user to have AI modify the output to meet their specific needs.

**Outcome and Experiences**:\
Market research was performed to identify a product fit, providing assitance in testing POCs (Proof of Concepts).

This project really educated me on the topic of AI and how it can be leveraged as a tool in my work and for the products I develop. This gave me insight into some of the technical aspects and best practices for leveraging AI.

The POC encountered some hallucination problems.

It was projected to greatly increase monthly output by 5-10%.

This project was downgraded as a priority by management at the approval stage for development. Another priority took precedence.

### Authentication Software

A strong authentication and authorization strategy is essential in a highly regulated industry.

- **Authentication** is the process of verifying the identity of a user.
- **Authorization** is the process of validating the actions allowed once authenticated.

**Problem**:\
There is no seperation between policy and code. No user group management strategy existed. Acess was provisioned through scripting to production data. Client tenants were provisioned access through IP whitelisting. This does scale and did not fit the model for software products managed.

The application software was a white-labeled product that data collection between a financial institution and their clients. IP whitelisting does not fit this model and would not allow for self-sign-up.

**Solution**:\
A third-party provider was utilized to offload security risk for authenticating users. Provider offered a solution for easily defining a role and assigning these roles to users.

**Outcome and Experiences**:\
Product was required to define user roles. To effectively define a role, a deep understanding of API authorization policy and user flow was required. Responsibilities also included the administrative functions during the client onboarding process. Product supported a quick iterable that included a T&C (Terms and Conditions) feature requiring custom HTML and CSS markup per client onboarded.

The application software was successfully taken to market. It offered self-sign-up capabilities with default role assignment that could be managed by an account admin.

**Lessons Learned**:\
I learned the importance of establishing boundaries for each cross-functional team. I have a lot of experience with establishing good communication with teams. This situation had me stretched between six engineering teams at the time. It was an overwhelming experience to be managing such scale early in my career. This team made a major architectural decision without discussing the impact. The decision presented a huge problem when taken to market that did not fit with the original vision.

The restriction resulted in poor experience for the account holders. A business can do business with multiple institutions. When our product was sold to more than one institution, it was very frustrating for account holders when the system rejected their sign-up attempts because they had a login with another financial instiution.

The refactor came at a great expense. It was at the end of this project when I discovered this as we were going to market.

### Banking Core

Banking core solutions are enterprise products for financial institutions. Features include new account creation, customer relationship management, interest calculations, deposits, withdrawals, loan issuing and servicing, etc.

> **Tip**: Follow this [link](https://www.ibm.com/topics/core-banking#:~:text=Core%20banking%20is%20the%20hub%2C%20or%20back-end%20connection%2C,accounts%2C%20deposits%2C%20and%20withdrawals%2C%20among%20other%20financial%20services.) for more information.

**Problem**:\
Loan boarding is the most time intensive task in commercial lending. Boarding is a post-closing activity (after the signing of loan documents) that requires a team to enter loan information into the banking core.

**Solution**:\
Integrating with banking cores provided real-time connectivity with origination software. Integration simplified the boarding process to a few clicks. This effectively decreased time spent from hours to minutes.

**Dependencies**:

- [Document Compliance Solution](#document-compliance-solution)
- Migration of reference data from constants files.
- Design of translation tables.

Dependencies had to be effectively managed in parallel, split into three seperate initiatives. The migration of reference data required deep insight into the three systems. This migration required a data design that would scale for the translation of data onboarded per client.

**Outcome and Experience**:\
The strategy consisted of two paths. Build it or buy it. Market research was performed by product to identify providers that offered a connector. The "buy it" strategy mitigated development cost. Integrations required development iterations per core provider. Connectors offered connectivity to multiple cores, requiring one integration.

The development of a custom connector was pursued. A third-party connector did not offer a suitable pricing strategy.

This was a great experience to drive an initiative of such magnitude. Core systems are extremely large systems that come with books of API documentation. I effectively documented API flows in layers for both systems (internal and external) that was essential to identifying requirements. This integration was primarily a backend project and consisted of few design requirements.

It was projected to increase output 10-15%. Most financial instituions do not have a dedicated role for this function. It was projected that business units could focus on other tasks with the decrease in time spent on this task.

I was repurposed during the development phase but played an essential role in the early stages that required months of planning and designing.

**Lessons Learned**:\
I previously had experience in leading integrations, but this project was much larger than previous integrations. These legacy systems had very poor documentation. The discovery process was time intensive. I learned the importance of documentation in our projects. Most documentation was non-existent; everybody had all the context needed. This effectively taught me to plan for good documentation. It is worth the time. This also taught me how to effectively navigate very poorly documented systems to mine the business requirements needed.

### Business Process Decision Modeling (BPM)

Workflow and decision automation software to create customizable workflows. Software orchestrates tasks based on defined business rules through automation.

**Problem**:\
The business marketed a strategy for two groups of people to live within one platform as one. Parties included internal business units that serviced overflow work and the client. Product workflow was originally designed to support software enabled services. It did not support the shift in strategy.

**Solution**:\
A BPM clearly separated work between the two groups by the business conditions defined in contractual agreements. This met the needs of the business to segregate the work for each responsible party. BPM also allowed the workflow to be customized by the client to fit their process.

**Outcome and Experience**:\
Market research was performed to review candidates for integration. Considerations included pricing, features, and product fit. This was a great experience to solve a difficult problem. This opportunity deepened my understanding of BPMs and design for business rules, task management, subscription of responsible parties, etc. I performed a lot of research and mocked several table designs for cross team collaboration.

This project was downgraded in priority by management at the approval stage for development. Another priority took precedence.

**Lessons Learned**:\
I had limited experience with BPM. I had experience as an end user in tools used. This was a great experience to learn about the data design concepts needed to support the concept problem faced. It was a great experience to ideate a user flow that had multi-facet personas.

### Document Compliance Solution

Document processing is the essential function of generating loan documents in lending. Compliance is pertinent to enforce binding agreements.

**Problem**:\
Entity, loan, and collateral data were duplicated in multiple systems.

**Solution**:\
A third-party offered an online stateless solution that allowed for data mapping and data transfer at launch.

**Outcome and Experience**:\
This solution decreased time to fund, margin of error, and created a path for additional integrations.

Responsibilities included API documentation and use case review. Compliance engine guaranteed legal compliance for all 50 states. The user flow was conditional, driven by their selection of data points. Business use case review identified a subset of the approximately one thousand supported data points for initial integration.

This required an intimate understanding of existing data and API design to facilitate the translation process from system to system. Business use cases were provided with API documentation to assist in the backend discovery process. This project required extensive testing and business review due to the compliance complexity.

Internal business units consumed this feature to service clients. This role was required to support the administrative activities and the client conversion from the pre-existing solution.

**Lessons Learned**:\
All projects required buy-in from stakeholders and customers. This experience included an environment with political factors and changing requirements. Business partners did not uphold their end of the deal. I had experience with this before, but I was able to lean on personal knowledge and research to meet deadlines. Loan documents presented so much risk, I was uncomfortable with leaning on personal experience and research. I learned how to effectively step back to navigate difficult situations to get the job done.

### Financial Statement OCR

Credit analysis requires calculation of repayment ability to make an informed decision for loan approval. Analysis is performed by financial statement review and data entry into cashflow models.

**What is OCR?**\
Optimal Character Recognition (OCR) is the procedure to transform a text image into a text format that can be read by a computer. This process can also be understood as scrapping. An example would include extracting data from a PDF document.

> **Tip**: Follow this [link](https://aws.amazon.com/what-is/ocr/) for more information.

**Problem**:\
Credit analysis requires the review of numerous tax returns of financial statements. Variation in deal complexity can require statement review ranging between three and thirty. This time intensive task requires more time to enter data instead of analyzing data.

**Solution**:\
A third-party provider offered a solution with OCR technology to extract the financial data from tax returns. Tax returns accounted for approximately 70% of financial statements recieved. Data elements extracted from PDFs were mapped to existing cashflow models, automating the data entry process.

**Outcome and Experiences**:\
Solution effectively decreased the average entry time of 45 minutes to 30 seconds. It significantly increased the output of the analyst function by 80%. The responsibilities of the analyst function were redefined. Monthly revenue was effectively raised by approximately 5-10%.

Provider's authentication and authorization policies were issued through API tokens. Tokens were internally managed by product, distributing access to tenant clients for a transparent experience to the end user. Provider deployed an API design that exposed an API for each data element. The definition of supported data elements was defined in a YAML file by API keys and labels by product.

Internal business units were consumers of this feature. Responsibilities included the design of the API mapping and administrative functions to set up live production cash models to support integrated OCR technology.

**Lessons Learned**:\
This was an earlier integration project, and I was still maturing my technical acumen. This project forced me to be a power user in postman. I simply used it for discovery before. This project deepened my understanding of APIs, postman, authentication, and more. This was a great experience that set the pace for me to develop the ability to self-educate in the world of technology.

### Industry Market Research

Industry data is essential to identify external factors. Factors are used to assess the health of business development plans. This is essential to issuing a risk rating to make an informed loan approval decision.

**Problem**:\
Relationship with existing vendor was diminishing due to their decrease in available data. The process required a user to login to their platform, search, print, and append file to another file. This manual step had room for error and required some training for analysts.

**Solution**:\
A third-party provider exposed APIs to extract data without following the traditional flow described in the problem statement. Integration would remove the manual step of searching and printing specific data points. Combining this integration with existing credit memo system, NAICS code stored for the entity would automatically retrieve applicable data during the credit memo stage in the workflow. It automated the appending of an industry analysis upon creating a final credit memo in PDF.

**Outcome and Experiences**:\
Product performed API research and documented flows for both systems. This was primarily a backend project that required little Design support. Product developed business cases and reviewed information with business units to identify most releveant information to priortize integration iterations.

It was projected to be a small time saver but it was really a convience factor. The vision was to decrease the time spent outisde of the platform.

This project was downgraded as a priority by management at the approval stage for development. Another priority took precedence.
