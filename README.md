# cfn-zookeeper
_AWS CloudFormation template for a highly-available Zookeeper cluster_

## Introduction
- Creates a three node cluster of Zookeeper instances managed by Exhibitor
- Shared storage provided by a dynamically created S3 bucket
- The cluster is fronted by a classic Load Balancer balancing on ports 2181 (Zookeeper clients) and 8080 (Exhibitor)
- Dynamic scaling up or down if the CPU utilization is greater than 90% or less than 70% for a period of one minute, respectively
- The stack outputs and exports the addresses of Zookeeper and Exhibitor which can then be used as inputs to other stacks
