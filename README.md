# AWS SNS Pipeline – CloudWatch, Lambda, and S3 Log Alerts

Overview
This project demonstrates how I built a log monitoring and alerting pipeline in AWS using:
- **CloudWatch Logs** for log collection
- **Lambda** for processing and forwarding events
- **SNS (Simple Notification Service)** for notifications
- **S3** for log storage and archiving

The goal is to simulate a real-world security/operations scenario where logs are monitored, stored, and alerts are generated automatically.

---

**Architecture**

EC2 Instance → CloudWatch Logs → Lambda → S3 + SNS → Email Alert

1. Configured CloudWatch Log Group to capture EC2 instance logs from /var/log/cloud-init.logs

2. Created Lambda Function to trigger on new log events and forward them.

3. Integrated SNS Topic to send notifications (email), incorporated with metrics for automation.

4. Created S3 Bucket to store and archive processed logs that aren't flagged as ERROR.

5. Tested with Custom Log Entries (echo "Test log entry" >> /var/log/cloud-init.log).

**Security Considerations**

- Applied least privilege IAM roles for Lambda and CloudWatch.

- S3 bucket configured with restricted access policies.
  
- Logs demonstrate awareness of monitoring & alerting best practices.

**Skills Demonstrated**

Cloud monitoring and logging (AWS CloudWatch)

Event Serverless processing (AWS Lambda)

Alerting and notification systems (SNS)

Secure log storage (S3)

Practical application of security monitoring & incident response concepts

**Contact**

Created by - **Theo Marques*

LinkedIn: https://www.linkedin.com/in/theo-marques-b3439b231/

GitHub: https://github.com/theopdmarques

Email: theopdmarques@gmail.com
