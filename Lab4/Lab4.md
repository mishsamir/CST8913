# Lab 4 Documentation

Introduction

This document provides a high-level plan for moving a two-tier web application to the cloud. The current system has two virtual machines: WebServerVM, which serves static content, and SQLVM, which hosts the backend SQL database. To improve availability and disaster recovery, we will deploy the application in multiple cloud regions with automatic failover and load balancing.

Architecture Diagram

![image](https://github.com/user-attachments/assets/69442713-efc1-44e6-a8da-8a6e0b346f68)

Key Components
 The application will run in at least two separate cloud regions for high availability.

A global load balancer will route traffic between regions.

Each region will have a regional load balancer to manage traffic within that region.


WebServerVM: Deployed in both regions behind their respective load balancers.

SQLVM: Uses active-passive replication, where one region has the primary database and the other has a read-replica ready to take over if needed.

Failover Mechanism:

If a region goes down, the global load balancer directs traffic to the healthy region.

Cloud-native database services will detect downtime and promote the replica to primary if necessary.
 Migration Steps
 Replicating Virtual Machines


Deploy WebServerVM and SQLVM in both target regions.

Ensure configurations remain consistent across all instances.
 Configuring Load Balancers


Deploy a global load balancer to direct traffic based on health checks.
Setting Up Database Replication & Failover

Configure SQLVM in the primary region as the main database.

Deploy SQLVM in the secondary region as a read-replica.

Use cloud-based database replication and failover services to automate role switching.
Testing and Validation

Run failover tests to confirm seamless redirection.

Verify data consistency between database replicas.

Conduct load testing to measure performance in a multi-region setup.
Deployment and Monitoring

Migrate the application during off-peak hours to reduce disruption.

Closely monitor performance and resolve any post-migration issues.
Conclusion

By moving to a multi-region cloud setup, the application will become more resilient and reliable. This migration minimizes downtime risks and ensures seamless failover, keeping the system operational even during regional failures. Leveraging cloud-native services allows for better scalability and performance.
