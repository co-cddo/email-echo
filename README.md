# **Email Echo Tester**

The **Email Echo Tester** is a serverless tool designed to help organisations validate their email authentication setups, including SPF, DKIM and DMARC; as well as demonstrate our BIMI configurations. Built on AWS infrastructure, the service ensures scalability, reliability, and cost efficiency while maintaining a secure and user-friendly experience.


## **Features**

- **Email Authentication Testing**  
  Analyse emails sent to the tester address for compliance with SPF, DKIM and DMARC standards.

- **Automated Response for Passing Emails**  
  Replies are sent only if the email passes all validation checks. The reply includes:  
  - A report of the validation results.  
  - The headers of the email sent for testing.

- **Serverless and Scalable**  
  Utilises AWS services for high performance and low cost:  
  - **Amazon Simple Email Service (SES):** Handles inbound and outbound email with robust email processing capabilities.  
  - **AWS Lambda:** Processes emails and runs validation logic efficiently without the need for dedicated servers.  
  - **Amazon S3:** Stores detailed test results for future testing and retrieval.  


## **How It Works**

1. **Send a Test Email**  
   Send an email from your domain to:  
   <test@email-echo.service.security.gov.uk>

2. **Validation and Analysis**  
   The tool analyses the email for:  
   - SPF alignment  
   - DKIM signature validation  
   - DMARC policy adherence

3. **Receive a Reply**  
   If the email passes all checks:  
   - A reply is sent containing the email's headers and a detailed validation report.  
   - If checks fail, the email is logged for review, but no reply is sent.


## **Why Serverless?**

The tool is built entirely using **Platform-as-a-Service (PaaS)** tools from AWS to ensure scalability, efficiency, and cost optimisation:  

- **Elastic Scaling:** Automatically adjusts to handle high volumes of emails without manual intervention.  
- **Reduced Costs:** Pay only for what you use—ideal for spiky or irregular usage patterns.  
- **Secure Processing:** Emails are processed securely within AWS, leveraging SES’s anti-spam and threat detection capabilities.  
