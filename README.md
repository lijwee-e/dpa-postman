# Postman Collection Request Sample for Data Protection Advisor

Dell EMC Data Protection Advisor (DPA) offers:
1. Monitoring and alerting of protection software and storage
2. Unified visibility across the data protection environments, on-premises and in the cloud
3. Simple self-service protection verification with single-click auditing
4. Comprehensive and flexible reporting
5. Scalable, centralized multi-tenancy for service level attainment

With its rich REST API capability, backup reporting can be extended to organisation’s workflow, such as chatbot, predictive analytics, and configuration management reporting.

Example:
https://www.linkedin.com/pulse/self-service-backup-reporting-chatbot-eng-li-jwee/

To get any report in DPA, you will need the following
1. The DPA Object ID
2. Report Name
3. Expected Duration

Tutorial example:
1. https://www.youtube.com/watch?v=iKvIuIvZP2E
2. https://www.youtube.com/watch?v=SNIgTPpFrpw

The REST API flow as follow:
1. Get Request - DPA Object ID
2. Post Request - Generate Report
3. Get Request - Download Report

![](images/DPA%20Flow.png)

Postman Request
 ![](images/sample-request.PNG)

To use the postman you will need to modify the following in the environment variable:
- url - The https://DPA Server IP:9002
- user_name - the credential you are using
  ![](images/Env-variable.PNG)
  
In each request under Authorization, you will need to modify to the password you are using.
  ![](images/Password.PNG)

To modify the hostname go to the request's pre-request of the "01-xxxxx" request
  ![](images/Pre-Request-Hostname.PNG)

To modfiy the report type go to the request's pre-request of the "02-xxxx" request
  ![](images/Pre-Request-Report-Name.PNG)
  
Run the request in the following sequence 01-Get-xxxx > 02-Post-xxxx > 03-Get-xxxx
![](images/sample-output.PNG)

