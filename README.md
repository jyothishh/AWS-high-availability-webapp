# AWS Highly Available and Auto-Scalable Web Application

## Project Overview

This project demonstrates how to deploy a web application on AWS using EC2, an Application Load Balancer, an Auto Scaling Group, and Amazon CloudWatch.

The objective is to improve application availability, distribute incoming traffic, and automatically adjust compute capacity based on demand.

## AWS Services Used

* Amazon EC2
* Application Load Balancer (ALB)
* Target Groups
* EC2 Auto Scaling
* Amazon VPC
* Amazon CloudWatch
* Linux and Apache

## Architecture

The Application Load Balancer distributes incoming HTTP requests across healthy EC2 instances. The Auto Scaling Group manages the number of instances, while CloudWatch monitors CPU utilization.

Add the architecture diagram here.

## Implementation Steps

1. Created a VPC and configured subnets.
2. Launched EC2 instances running Apache.
3. Created a Target Group and configured health checks.
4. Created an Application Load Balancer.
5. Configured a launch template for EC2 instances.
6. Created an Auto Scaling Group.
7. Configured a CPU-based scaling policy.
8. Used CloudWatch to monitor CPU utilization and scaling activity.
9. Tested website accessibility and instance replacement.

## Testing and Results

Document the actual results of your tests:

* Load balancer website access: Apache default page loaded through the load balancer dns
* Target Group health checks: Shows 1 healthy target
* CPU-based scaling test: Auto Scaling adjusts the number of EC2 instances when required by the scaling policy.
* Instance replacement test: A replacement instance launches and becomes healthy.

## Security

* Restricted inbound traffic using security groups.
* Allowed web traffic through the Application Load Balancer.
* Configured instance access according to the project's security requirements.

## Cost Management

AWS resources were monitored during testing. Unnecessary billable resources were removed after testing.

## Learning Outcomes

* AWS compute and networking fundamentals
* Load balancing and health checks
* Auto Scaling configuration
* CloudWatch monitoring
* Linux server administration
* Troubleshooting AWS infrastructure
