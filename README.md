# cfn-zookeeper
_AWS CloudFormation template for a highly-available Zookeeper cluster_

## Introduction
- A three node cluster of Zookeeper instances managed by Exhibitor with shared storage provided by an S3 bucket.
- The cluster is fronted by a classic Load Balancer balancing on ports 2181 (Zookeeper clients) and 8080 (Exhibitor).
- The cluster will dynamically scale up or down if the CPU utilization is greater than 90% or less than 70% for a period of one minute.
