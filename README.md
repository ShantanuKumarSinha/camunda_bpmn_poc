# Camunda BPMN with Spring Boot and PostgreSQL

This application is to showcase how to use camunda bpmn

### What is Camunda?
    Camunda is an open-source platform for workflow and decision automation. It provides a suite of tools
    for modeling, executing, and monitoring business processes using BPMN. Camunda allows you to define
    business processes in a standardized way and execute them in a scalable and reliable manner.

### What is BPMN?
    BPMN (Business Process Model and Notation) is a standard for business process modeling that
    provides a graphical representation of business processes. It is designed to be easily understandable by all stakeholders, including business analysts, technical developers, and business managers.

### What is Spring Boot?
    Spring Boot is an open-source Java-based framework used to create stand-alone, production-grade Spring-based applications. It simplifies the setup and development of new applications by providing a range of pre-configured features and dependencies.

### What is Java 17?
    Java 17 is a long-term support (LTS) version of the Java programming language, released in September 2021. It includes significant improvements and new features over previous versions, such as enhanced pattern matching, sealed classes, and new APIs for better performance and security. Java 17 is widely used for building modern applications due to its stability and support. 

### What is PostgresSQL?

    PostgreSQL is a powerful, open-source object-relational database system that uses and extends the SQL language. It is known for its robustness, extensibility, and support for advanced data types and performance optimization features. PostgreSQL is widely used for web applications, data warehousing, and other data-intensive applications.


### Tools used:

- Camunda Modeler
- Camunda Platform
- Spring Boot
- Java 17
- Rest API
- PostgresSQL
- Maven

What we are going to build

    We will build a simple Spring Boot application that uses Camunda BPMN to model and execute a business process. The application will include a REST API to interact with the process and a PostgreSQL database to store process data.

How do we achieve this?

1. **Set up the Spring Boot application**: Create a new Spring Boot project with the necessary dependencies for Camunda, PostgreSQL, and REST API.
2. **Model the BPMN process**: Use Camunda Modeler to create a BPMN diagram that defines the business process. This diagram will include tasks, gateways, and events that represent the flow of the process.
3. **Configure Camunda in Spring Boot**: Integrate Camunda into the Spring Boot application by adding the necessary configuration files and dependencies. This will allow the application to execute the BPMN process defined in the modeler.
4. **Implement REST API endpoints**: Create REST API endpoints to start the process, query process instances, and complete tasks. These endpoints
5. **Connect to PostgreSQL**: Configure the application to connect to a PostgreSQL database for storing process data. This will involve setting up the database connection properties and creating the necessary tables.
6. **Run the application**: Start the Spring Boot application and test the REST API endpoints to ensure that the BPMN process can be executed and managed through the API.
7. **Monitor the process**: Use Camunda's built-in monitoring tools to track the execution of the BPMN process, view active instances, and analyze performance metrics.


References:
- Camunda Documentation : 
    (https://docs.camunda.org/)https://4513465.fs1.hubspotusercontent-na1.net/hubfs/4513465/EN-Camunda-Compared-to-Alternatives-2024.pdf






### Changes in UPI Payment Gateway

	* Daily Limit on balance check 
        Daily balance check via UPI limited to 50 times per day(per app).
	* Limit on Account Listing API 
        UPI apps can call the "List Accounting" API (to show linked accounts) only 25 times/day per usage.
	* Failed Transaction retry limit 
        If a upi payment fails only 3 retry per transaction. It will be restricted during peak hours
	* AutoPay Time Slot Enforced
        UPI Auto pay will be carried out in fixed time windows, Mostly non peak hours.
	* API Rate Controls: Banks and Payment Service provides must set control on 
		TPS(Transaction/sec) 
		Velocity(frequency of apis)
        Ensuring rate limit is applied on client side
	* Streamlining refund and chargable rules
	* UPI Aggregator Charges (Back-end only)
		Payment Aggregator now needs to payback small charges (This may impact processing fees)

- Objective

    The changes are implemented by the National Payments Corporation of India (NPCI) to enhance the stability and reliability of the UPI ecosystem. These measures are aimed at reducing congestion during peak hours, ensuring fair usage of resources, and improving the overall user experience.

-Technical Implementation

    Implement rate limiting on the UPI APIs to control the number of requests made by users and applications. This involves setting limits on the number of requests per user, per application, or globally across the system. The rate limit can be enforced using various techniques such as token buckets, leaky buckets, or fixed window counters.
    The rate limit is implemented to control the number of requests made to the UPI APIs. This is done to prevent abuse and ensure fair usage among all users. The rate limit can be applied at various levels, including per user, per application, or globally across the system.

- Technical Achievements
    * Less congestion during peak hours
    * Less API calls
    * Less load on servers
    * Less data transfer
    * Less processing time
    * Less latency in transactions
    * Less server replicas 
    * Reduces cost of infrastructure
    * Reduces downtime
