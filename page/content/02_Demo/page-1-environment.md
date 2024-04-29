---
title: "The environment"
weight: 31
---
## Architecture

We’ve prepared an AWS + Elastic environment for you. Within the AWS environment there is a simple python application deployed on EC2. This application accesses DynamoDB and uses Lambda functions to enrich an object with more information. All the monitoring information including metrics and logs from the entire system are collected in Elastic. This is done by using one Elastic Agent at the EC2 instance and the Elastic Serverless forwarder for the logs. While the Elastic Agent would also be able to collect the different log types, this architecture has the advantage of running log monitoring on different hardware. 

The architecture of the sample app looks like this. For better load distribution we have two EC2 instances running. One is called Elastic-Agent and one is called Elastic-App.
![Elastic environment](/images/aws_workshop_arch.png)

While running the workshop you have access to your Elastic Cluster and to the EC2 instances that are running the application. In your Elastic Cluster you can find a dashboard called **Workshop Dashboard**. Use this dashboard as a starting point for all your tasks. You can solve all the tasks by using these components. You don’t need anything else.
Your task is to find the issues using the Elastic Cluster and to fix the issues within the EC2 environment(s).

The code that is running the application is downloaded from this [GitHub Repo](https://github.com/bct-timo-crabbe/aws-workshop) to the EC2 environment(s). If you like 
