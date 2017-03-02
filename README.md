# cfn-zookeeper
_AWS CloudFormation template for a highly-available Zookeeper cluster_

## Features
- Three node auto-scaling cluster of Zookeeper instances
- Dynamic configuration managed by Exhibitor with S3
- Load Balancer balancing on ports 2181 and 8080
- Exports the addresses of Zookeeper and Exhibitor
