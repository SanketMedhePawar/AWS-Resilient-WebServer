# 🚀 AWS Resilient Web Server Project

This project demonstrates a resilient, self-healing, and auto-scaling web server architecture on AWS using EC2, Auto Scaling Groups, Load Balancer, and monitoring tools.

---

## 🛠️ Key AWS Services Used

- **VPC** (with Subnets, Internet Gateway, Route Tables)
- **EC2** (Amazon Linux 2 with Apache installation via Launch Template)
- **Auto Scaling Group** (based on CPU utilization)
- **Elastic Load Balancer (ELB)** for traffic distribution
- **CloudWatch** for monitoring and alarms
- **SNS** for notifications
- **IAM Roles** for secure access
- **S3** (optional - for hosting assets like bootstrap templates)

---

## 📸 Implementation Screenshots

All setup steps with screenshots are included in the PDF below:

👉 [Download screenshots.pdf](./screenshots.pdf)

---

## 📈 Architecture Diagram

         ┌────────────┐
Users ───▶│ Elastic Load│
│ Balancer │
└────┬───────┘
│
┌────────────┼────────────┐
┌───▼───┐ ┌───▼───┐ ┌───▼───┐
│ EC2-1 │ │ EC2-2 │ │ EC2-3 │ (Auto Scaling Group)
└───────┘ └───────┘ └───────┘
│ │
┌────┴──────────────┴─────┐
│ CloudWatch + SNS Alerts │
└──────────────────────────┘
│
┌────┴────┐
│ S3 │ (optional)
└─────────┘
