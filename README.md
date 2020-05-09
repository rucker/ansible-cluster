# Ansible Cluster
Ansible playbooks to provision compute cluster nodes

## Assumptions
- Compute cluster consists of 4 nodes: A head node and 3 nodes gatewayed behind it using the private subnet 192.168.50.[1-4]
- Any networking requirements are met and interfaces are configured
- The desired user exists, ssh key auth configured on all cluster nodes

## Requirements
- The following environment variables should be set:
  - `CLUSTER_HEAD_NODE`, `CLUSTER_NODE_2`, `CLUSTER_NODE_3`, and `CLUSTER_NODE_4`: The cluster hostnames
  - `CLUSTER_USER`: The user who will perform actions on cluster hosts
  - `CLUSTER_SSH_KEY`: The SSH key used to authenticate the cluster user
