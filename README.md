# aws-ansible-palybooks
This repository contains the ansible playbooks for automating aws infrastructure resources

# Playbooks
# 1. launch_ec2.yaml 
       - run this to instantly launch an amazon linux ami ec2 instance
# 2. vpc_launch.yaml
       - creates a VPC with a public subnet and  two private subnets
       - creates a internet gateway for public conectivity
       - creates an nat gateway and add nat routing entry for private subnets
# 3. vpc_peering.yaml
       - creates two VPC's within same account with non-overlapping CIDRs
       - creates one public subnet for each VPC
       - creates Internet gateway and add rouing entries for public subnets
       - create security groups in in each subnet for allowing ssh from anywhere and http and icmp traffic from peered VPC
       - creates a vpc peering connection 
       - accepts the peering connection
       - updates the routing table for both the subnets to allow traffic via peering connection
