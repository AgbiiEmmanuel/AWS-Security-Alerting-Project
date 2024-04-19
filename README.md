# AWS-Security-Alerting-Project
Welcome to the AWS Security Alerting Project! This project aims to provide a straightforward setup for monitoring and receiving alerts for security events within your AWS environment, utilizing services such as GuardDuty, Simple Notification Service (SNS), and CloudWatch. This Readme file will guide you through the setup process and explain how the different components work together to enhance the security posture of your AWS account.


![Security Alaerting AWS Project](https://github.com/AgbiiEmmanuel/AWS-Security-Alerting-Project/assets/159606680/a5c6b249-2410-486d-9e51-fed1eb1ea339)

# Setup Intructions:
1. ## Create an AWS Account:
If you haven't already, create an AWS account at [Amazon Web Services](https://aws.amazon.com/)

2. ## Enable Amazon GuardDuty:
* Log in to your AWS Management Concole.
* Search for "GuardDuty" and enable it for your account.

3. ## Set Up Simple Notification Service (SNS):
* In the AWS Management Console, search for "SNS" (Simple Notification Service).
* Create a new topic named "GuardDuty" to receive GuardDuty alerts.
* Create a subscription under the "GuardDuty" topic, providing your phone number or email address to receive alerts.

4. ## Configure CloudWatch Alarm:
* In the AWS Management Console, search for "CloudWatch".
* Create a custom rule specific to GuardDuty events.
* Set the target of the rule to the "GuardDuty" SNS topic created earlier.
* This CloudWatch alarm will trigger whenever GuardDuty detects security events and send alerts to the subscribed phone number or email.

5. ## Configure GuardDuty Sample Alerts:
* In GuardDuty settings, create sample alerts to simulate various security threats.
* These sample alerts will trigger the CloudWatch alarm, which in turn will notify you via the configured SNS subscription.
# Customization Options:
## Adjusting Alert Severity:
* Within the CloudWatch rule, you can customize the severity level of alerts to be forwarded to SNS. This allows you to filter out less critical events and focus on high-priority security threats.
## Fine-tuning GuardDuty Settings:
* Explore GuardDuty settings to adjust sensitivity levels and fine-tune the types of security events that trigger alerts.
## Expanding Alert Notifications:
* Extend the SNS subscription to include additional recipients or channels for alert notifications, ensuring that the right people are informed promptly in the event of a security incident.

# Security Considerations:
## Secure Access to AWS Account:
* Ensure that access to your AWS account is secured with strong authentication mechanisms and follows the principle of least privilege.
## Regular Monitoring and Review:
* Regularly monitor GuardDuty findings and review alert notifications to stay informed about potential security risks in your AWS environment.
## Continuous Improvement:
* Continuously assess and refine your security alerting setup to adapt to evolving threats and improve incident response capabilities.

# Conclusion:
By following these setup instructions and leveraging AWS services like GuardDuty, SNS, and CloudWatch, you can establish a robust security alerting system for your AWS environment. Prompt detection and response to security incidents are crucial for maintaining the integrity and confidentiality of your resources, and this project aims to simplify the process of setting up such capabilities.

Thank you for choosing the AWS Security Alerting Project. If you have any questions or encounter any issues during setup, feel free to reach out to me for assistance.

Happy alerting and stay secure!
