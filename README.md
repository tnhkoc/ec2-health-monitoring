# EC2 CPU Utilization Alarm with SNS Notification

This project demonstrates how to create a CloudWatch alarm for high CPU utilization on an EC2 instance and notify via Amazon SNS.

## 🛠️ Services Used

- Amazon EC2
- Amazon CloudWatch
- Amazon SNS

## 🔧 Project Steps

### 1. Create SNS Topic and Subscription

Create a new SNS topic and subscribe with your email to receive alarm notifications.

**Screenshots:**
- ![Create SNS Topic](screenshots/sns-create-topic.png)
- ![Create SNS Subscription](screenshots/sns-subscription-create.png)
- ![Confirm Email Subscription](screenshots/sns-alarm-notification-email.png)

### 2. Create CloudWatch Alarm

Select the EC2 instance metric (CPU Utilization) and set the conditions.

**Screenshots:**
- ![Select Metric](screenshots/cloudwatch-alarm-select-metric.png)
- ![Define Conditions](screenshots/cloudwatch-alarm-define-conditions.png)
- ![Select SNS Topic](screenshots/cloudwatch-alarm-select-sns-topic.png)

### 3. Simulate High CPU Load

SSH into your EC2 instance and simulate load using the `stress` tool to trigger the alarm.

**Screenshot:**
- ![Stress Test](screenshots/ec2-cpu-stress-test-terminal.png)

## 📬 Alarm Notification

When the threshold is breached, you will receive an email from SNS.

**Screenshot:**
- ![Alarm Notification](screenshots/sns-alarm-notification-email.png)

## ✅ Result

CloudWatch successfully detects the high CPU usage and notifies the subscriber via SNS.
