# Hadoop Cluster Setup with Ansible

This repository contains Ansible playbooks to automate the setup of a Hadoop cluster. The playbooks cover installation of prerequisite packages, configuration of Hadoop services, and setting up Spark on top of Hadoop.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
  - [Configure HDFS](#configure-hdfs)
  - [Configure YARN](#configure-yarn)
  - [Configure Spark](#configure-spark)
- [SSH Key Distribution](#ssh-key-distribution)

## Prerequisites

The playbooks ensure that the necessary packages are installed based on the operating system distribution.

### RHEL Compatible Distributions
- `wget`
- `java-11-openjdk-devel`
- `tar`

## Installation

The installation playbook downloads and extracts the Hadoop tarball to `/opt`.

## Configuration

The configuration playbooks set up the necessary environment variables and configure Hadoop, HDFS, YARN, and Spark.

### Configure HDFS

The HDFS configuration playbook sets various properties such as replication factor, data directories for the NameNode and DataNodes, and other essential configurations for a distributed storage system.

### Configure YARN

The YARN configuration playbook sets up resource management properties like memory allocation, enabling ACLs, and specifying the ResourceManager hostname to facilitate job scheduling and cluster resource management.

### Configure Spark

The Spark configuration playbook customizes environment settings such as `HADOOP_CONF_DIR` and `SPARK_DIST_CLASSPATH`, ensuring proper integration with Hadoop. It also configures default properties like memory allocation for Spark applications.

## SSH Key Distribution

The playbooks handle the generation and distribution of SSH keys for passwordless authentication among master nodes, facilitating seamless communication within the Hadoop cluster environment.