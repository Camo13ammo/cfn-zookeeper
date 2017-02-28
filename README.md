# cfn-zookeeper
_AWS CloudFormation template for a highly-available Zookeeper cluster_

## Features
- Creates a three node cluster of Zookeeper instances managed by Exhibitor.
- Shared storage provided by a S3 bucket.
- Fronted by a Load Balancer balancing on ports 2181 (Zookeeper clients) and 8080 (Exhibitor).
- Dynamic scaling based on CPU utilization; greater than 90% or less than 70% for a period of one minute.
- Exports the addresses of Zookeeper and Exhibitor.
