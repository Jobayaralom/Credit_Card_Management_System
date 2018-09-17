# Credit_Card_Management_System
Credit Card Management System
Release ID: QTAD-SRDUC.doc / 1.0 /
  
  Controlled copy Software Requirements Document
1 Introduction
1.1 About this document
1.1.1 Purpose & Scope of the document
The purpose of the software requirements document is to systematically capture requirements for the project and the system “Credit Card System” to be developed. Both functional and non-functional requirements of this system are captured in this document. It also serves as the input for the project scoping.
The scope of this document is limited to addressing the requirements from a user, quality, and non-functional perspective. It is recommended that design aspects are not added in this document
1.1.2 Intended Audience
Project Team
1.2 About the Software System
The following section will cover aspects related to
Credit Card System (CCS) application. A credit card is a payment card issued to users as a system of payment. It allows the cardholder to pay for goods and services based on the holder's promise to pay for them.The Credit Card Products will include the following fields that can be adjusted and viewed by the managers of the Bank:
The following are the modules in this proposed system
a) Customer Details. b) Transaction Details.
1.2.1 Scope of the system
The scope of the system is explained through its modules as follows
 Customer Details -- This Module will be used by the Bank admin to register the existing Customer details into the system. The bank admin should have the details of the Customers to be entered into the system.
 Transaction Details - This Module will be used by bank admin to enter the bank details received upon a request approval from admin. The system should then update the Customer details in the system along for the corresponding Customer.
1.2.2 Exclusions
1. The system will operate only on the modules discussed above and will not include
Credit Card System <SCI.ID. > / Ver: <Ver No.> Release ID: QTAD-SRDUC.doc / 1.0 / C3: Protected Page 4 of 10
   
  Controlled copy Software Requirements Document
any additional functionality.
1.2.3 SystemPerspective
The Credit Card System is an independent software system developed to manage the activities like Registering New Customer, approving or cancelling the request, etc. using the architecture.
1.2.4 SystemEnvironment 1.2.5 Architecture diagram
Physical Architecture:
A physical architecture is an arrangement of physical elements, (system elements and physical interfaces) that provides the designed solution for a product, service, or enterprise. It is intended to satisfy logical architecture elements and system requirements. Auto Identification Process follows a three layered architecture namely presentation layer, business logic layer and data access layer.
 Logical Architecture:
The Logical Architecture defines the Processes (the activities and functions) that are required to
Credit Card System <SCI.ID. > / Ver: <Ver No.> Release ID: QTAD-SRDUC.doc / 1.0 / C3: Protected Page 5 of 10
   
  Controlled copy Software Requirements Document
provide the required User Services. Many different Processes must work together and share information to provide a User Service. The Processes can be implemented via software, hardware, or firmware. The Logical Architecture is independent of technologies and implementations.
 1.2.6 Impact of the System
This is a new product which is developed for internal users. Expected impact of the product is to automate existing manual processes in order to make them more efficient and cost effective.
1.2.7 Assumptions, Risks / Constraints
Assumptions:
1. The processing admin must possess prior knowledge on Credit Card System
operations
2. The admin should have the details of the Customers to be registered for applying credit card updated into the system.
1.2.8 Design Constraints – from the template
1. The customer details module and the Transaction details modules should remain
Credit Card System <SCI.ID. > / Ver: <Ver No.> Release ID: QTAD-SRDUC.doc / 1.0 / C3: Protected Page 6 of 10
   
  Controlled copy Software Requirements Document
independent, without affecting credit card System.
 Credit Card System <SCI.ID. > / Ver: <Ver No.> Release ID: QTAD-SRDUC.doc / 1.0 / C3: Protected Page 7 of 10
  
  Controlled copy Software Requirements Document
2 System Requirements
2.1 Functional Requirements –excel mapping
2.1.1 Transaction Details Module
1.1.1 Transaction Details
   Credit Card System
   Customer Details
   Req-2.1.1
        Functional Requirements
  1) To display the transactions made by customers living in a given zipcode for a given month and year. Order by day in descending order.
2) To display the number and total values of transactions for a given type.
3) To display the number and total values of transactions for branches in a given state
       2.1.2 Customer Details Module
1.1.2 Customer Details
     Credit Card System Req-2.1.2
      Customer Details
        Functional Requirements
  1) To check the existing account details of a customer.
2) To modify the existing account details of a customer
3) To generate monthly bill for a credit card number for a given month and year.
4) To display the transactions made by a customer between two dates. Order by year, month, and day in descending order.
     Credit Card System <SCI.ID. > / Ver: <Ver No.> Release ID: QTAD-SRDUC.doc / 1.0 / C3: Protected Page 8 of 10
  
 
Controlled copy Software Requirements Document
2.2 Functional Requirements – ETL of Data
2.2.1 Data Extraction and Transportation Module
2.2.1.1 Data Extraction and Transportation with Sqoop
 
Credit Card System Req-2.2.1
 
 
Data Extraction and Transportation with Sqoop
 
Functional Requirements
Utilize Sqoop to extract the following data according to the specifications found in the mapping document:
1. Branch data into CDW_SAPP_BRANCH.txt
2. Credit Card Data into CDW_SAPP_CREDITCARD.txt
3. Time data into CDW_SAPP_TIME.txt
4. Customer Data into CDW_SAPP_CUSTOMER.txt
Notes:
 Data Engineers will be required to transform the data based on requirements found in the Mapping Document prior to loading the data into Hadoop.
 TIMEID is a field that the Data Engineers should create based on the DAY, MONTH, and TIME fields located in the CUSTOMER table. Format should be YYYYMMDD. For instance, January 4th, 2017 would become 20170104
 Data Engineers should extract the above data to the /Credit_Card_System/ folder in the Hadoop Filesystem
2.2.2 Data Loading Module

