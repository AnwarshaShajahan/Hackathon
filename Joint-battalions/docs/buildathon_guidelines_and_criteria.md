# **Buildathon – Guidelines & Criteria**

# **1\. Buildathon Overview**

The Buildathon is a project-based development challenge where teams will be provided with a **Product Requirements Document (PRD)** at the beginning of the Buildathon.

The PRD will define the required product, features, functionalities, workflows, and other project requirements.

Teams are expected to study and understand the PRD and implement the complete product according to the given requirements.

There is **no fixed application development stack** for the Buildathon. Teams are free to choose the programming languages, frameworks, libraries, and other technologies they consider appropriate.

However, there is a **mandatory requirement for the database technology**, which is explained below.

### **Expected Application Structure**

Each team is expected to build:

* **1 Backend / Server-Side Application**  
* **2 Web Applications / Web Access Interfaces**  
* **1 Mobile Application**  
  * Cross-platform mobile development is preferable.

# **2\. Team Structure**

### **Team Size**

* **Minimum:** 3 members  
* **Maximum:** 5 members

### **Mandatory Team Structure**

The minimum team structure must consist of:

* **2 Web Developers**  
* **1 Mobile Developer**

This **2 : 1 structure is mandatory for the minimum 3-member team**.

Teams may have up to 5 members. Additional members can be assigned based on the requirements of the project and the team's implementation needs.

### **Example Team Structures**

**3 Members — Minimum**

* 2 Web Developers  
* 1 Mobile Developer

**4 Members**

* 2 Web Developers  
* 1 Mobile Developer  
* 1 Additional Developer / Role

**5 Members — Maximum**

* 2 Web Developers  
* 1 Mobile Developer  
* 2 Additional Developers / Roles

The additional members may contribute to areas such as backend development, frontend development, mobile development, testing, DevOps, security, database, or other project requirements.

### **Mobile Developer**

A dedicated Mobile Developer is expected as part of the team.

However, if a team is able to build the mobile application without a dedicated Mobile Developer, the team may still proceed.

In such cases, the team must be capable of:

* Properly explaining the mobile application.  
* Explaining the technologies used.  
* Understanding the application's architecture.  
* Handling bugs and issues.  
* Implementing required security fixes and patches.  
* Maintaining and demonstrating the mobile application during the final evaluation.

### **Cross-Platform Mobile Development**

Cross-platform mobile development is **preferable**.

Teams may use technologies such as:

* React Native  
* Flutter  
* .NET MAUI  
* Or any other suitable cross-platform technology.

There is no mandatory mobile technology.

# **3\. Product Requirements Document (PRD)**

The **PRD will be provided when the Buildathon begins**.

The PRD will be the primary reference for understanding what needs to be implemented.

Teams are expected to:

* Carefully read and understand the PRD.  
* Identify all required functionalities.  
* Understand the expected user workflows.  
* Implement the requirements mentioned in the PRD.  
* Clarify requirements when necessary.  
* Ensure that the final implementation matches the expected requirements.

### **Important**

Teams should not simply focus on building individual features.

The objective is to implement the **complete product described in the PRD**, including the required backend, web applications, and mobile application.

If a requirement in the PRD is unclear, teams should seek clarification through the appropriate Buildathon communication channel before making major implementation decisions.

# **4\. Technology Stack**

There is **no fixed technology stack** for the Buildathon.

Teams are free to select the technologies, programming languages, frameworks, and libraries that best suit the requirements defined in the PRD.

However, the following database requirement is **mandatory**.

## **Mandatory Database Requirement**

### **SQL Database is Compulsory**

Teams **must use an SQL-based relational database** as the primary database for the project.

Acceptable examples include:

* PostgreSQL  
* MySQL  
* Microsoft SQL Server  
* SQLite  
* Oracle Database  
* Or any other suitable SQL-based relational database.

**NoSQL databases cannot be used as the primary database.**

Examples of NoSQL databases include:

* MongoDB  
* DynamoDB  
* Cassandra  
* CouchDB  
* etc.

Teams may use additional technologies such as Redis for caching or other supporting purposes where appropriate, but the **primary application database must be SQL-based**.

# **5\. Database Design Submission**

The database design must be prepared and submitted during the initial stage of the Buildathon.

### **Submission Deadline**

**Database Design must be submitted within the first 2 days of the Buildathon.**

This requirement is mandatory.

The database design should be based on the requirements provided in the PRD.

### **Database Design Should Include**

Depending on the project requirements, the submission should include:

* Entity identification  
* Tables  
* Columns / attributes  
* Primary keys  
* Foreign keys  
* Relationships  
* Constraints  
* Appropriate data types  
* Normalization considerations  
* Relationship cardinality  
* ER Diagram / ERD  
* Any important database design decisions

The submitted design should demonstrate that the team has understood the data requirements of the PRD and has planned the database structure before proceeding deeply into implementation.

> **Important:** Teams should not wait until the end of the Buildathon to design the database. The database design must be submitted within the first 2 days.

# **6\. Buildathon Phases**

The Buildathon will be conducted in **two phases**.

## **Phase 1 – Implementation Phase**

**Duration: 4 Weeks**

During the first phase, teams will implement the product based on the provided PRD.

Teams are expected to:

* Understand the PRD.  
* Prepare and submit the database design within the first 2 days.  
* Implement the backend.  
* Implement the required web applications.  
* Implement the mobile application.  
* Integrate all applications with the backend.  
* Implement the required functionalities and workflows.  
* Handle authentication and authorization where required.  
* Follow appropriate security practices.  
* Test the implementation.  
* Identify and fix bugs.  
* Maintain proper documentation.  
* Maintain the project using Git/version control.  
* Keep the implementation aligned with the PRD.

### **Phase 1 Review**

At the end of Phase 1, the projects will be reviewed.

Teams may be shortlisted for Phase 2 based on factors such as:

* Completion of required functionalities  
* Correct implementation of the PRD  
* Application stability  
* Number and severity of bugs  
* Code quality  
* Architecture  
* Security practices  
* Database design and implementation  
* Documentation  
* Integration between backend, web, and mobile applications  
* Overall project completeness

> **Important:** Completing more features does not automatically mean a better project. Correctness, stability, quality, and adherence to the PRD are important.

# **7\. Phase 2 – Bug Fixing & Finalisation**

**Duration: 1–2 Weeks**

Teams shortlisted after Phase 1 will proceed to Phase 2\.

The primary objective of Phase 2 is to **stabilize and finalize the implementation**.

Teams will work on:

* Fixing identified bugs.  
* Fixing security issues.  
* Resolving functional issues.  
* Improving existing implementations.  
* Fixing UI/UX issues where required.  
* Applying necessary patches.  
* Improving application stability.  
* Completing documentation.  
* Performing final testing.  
* Preparing the final demonstration.  
* Preparing the final presentation.

Teams should focus on making the application **stable, reliable, and ready for final evaluation**.

# **8\. Final Presentation**

At the end of Phase 2, shortlisted teams will present their project.

The presentation should clearly demonstrate the implementation based on the PRD.

### **Teams should explain:**

#### **Product Understanding**

* What is the purpose of the product?  
* What problem does the product solve?  
* Who are the intended users?  
* What are the major workflows?

#### **Technical Implementation**

* Backend architecture  
* Web application architecture  
* Mobile application architecture  
* Database architecture and design  
* API implementation  
* Authentication and authorization  
* Security considerations  
* Important technical decisions

#### **Working Demonstration**

Teams must demonstrate the **actual working application**.

The demonstration should cover the major functionalities and workflows defined in the PRD.

#### **Team Contribution**

Every team member should be able to explain:

* Their responsibilities.  
* The components they worked on.  
* The technical decisions they made.  
* The challenges they faced.  
* How they solved those challenges.

# **9\. Evaluation Criteria**

The final evaluation will consider the overall quality of the implementation.

Important areas include:

* **PRD Compliance**  
* **Functionality**  
* **Application Stability**  
* **Bug Handling**  
* **Code Quality**  
* **Architecture**  
* **Database Design**  
* **Security**  
* **UI/UX**  
* **Backend Implementation**  
* **Web Application Implementation**  
* **Mobile Application Implementation**  
* **API Design**  
* **Documentation**  
* **Team Collaboration**  
* **Technical Understanding**  
* **Final Presentation**  
* **Overall Completeness**

The evaluation will focus on how effectively the team converts the **provided PRD into a working software product**.

# **10\. Documentation Requirements**

Teams are expected to maintain proper documentation throughout the Buildathon.

Documentation may include:

* Project setup instructions  
* Architecture documentation  
* API documentation  
* Database documentation  
* ER Diagram  
* Environment configuration  
* Installation instructions  
* Deployment instructions  
* Important technical decisions  
* Known issues  
* Testing information  
* Security considerations

Documentation should be maintained throughout the development process rather than being created only at the end.

# **11\. Security**

Security should be considered throughout the implementation.

Teams should pay attention to areas such as:

* Authentication  
* Authorization  
* Input validation  
* API security  
* Data protection  
* Secure password handling  
* Token/session security  
* Access control  
* Secure file handling  
* Environment variables and secrets  
* Common web/mobile security vulnerabilities

Teams should also be able to explain the security measures implemented in their project during the final presentation.

# **12\. Prize**

🏆 **Buildathon Winner – Cash Prize: ₹1,00,000**

The final winning team will receive a **cash prize of ₹1,00,000**.

The winner will be selected based on the overall evaluation of the implementation, technical quality, stability, security, documentation, team understanding, and final presentation.

# **13\. Important Expectations**

The Buildathon should be approached as a **real-world software implementation project**.

Since the PRD will already be provided, teams should focus on:

**Understand the PRD → Design the Database → Implement → Integrate → Test → Fix → Document → Present**

Teams should ensure that:

* The implementation follows the PRD.  
* The database is SQL-based.  
* The database design is submitted within the first 2 days.  
* The major functionalities are properly implemented.  
* The applications work together correctly.  
* Bugs are identified and fixed.  
* Security is considered.  
* Documentation is maintained.  
* Every team member understands the project.  
* The final application can be properly demonstrated.  
* The team can explain the technical decisions made during implementation.

# **14\. Final Reminder**

The Buildathon is not only about completing the required functionalities.

Teams are expected to demonstrate their ability to take a **predefined product requirement and turn it into a complete, functional, secure, maintainable software product**.

The **PRD defines what needs to be built**.

The **team is responsible for deciding how to build it effectively**.

### **Core Process**

**PRD Understanding → Database Design → Implementation → Quality → Security → Testing → Documentation → Bug Fixing → Final Presentation**

Every team member should have a clear understanding of the complete project and should be able to confidently explain their contribution and the technical implementation.

