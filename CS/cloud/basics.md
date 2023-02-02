# Cloud

## IAAS

I retain the complete control

I pay for the resources I use

Not paying for when I am not using it

Whole bunch of responsibility

They provide the

      hardware

      Storage

      Network

      Compute

      Aws EC2, compute engine GCP

## PAAS

### Elastic beanstalk AWS

I have application code and use this and run

They take care of the os, scalling, availability

## Saas

Consuming a software as service

    Eg dropbox

    Ms word 365

### Public cloud

Delivered via the internet

Shared by many organisations

### Private cloud

Dedicated on premises hardware

Used exclusively by single organisation

### Hybrid

Combines private and public cloud

Vpn or dedicated connection(Aws direct connect)

## Cloud Infrastructure

### Regions

Geographic area (US East)

Will have multiple availability zones

### Availability Zones

There are more than 1 data centers

Shared by 1 power grid

So we will deploy our application in webserver to different availability zones so that if one fails other will help

### Edge Location

Content will be cached in edge location

So that user can use application faster

Edge location near to user will receive the request

#### Hypervisor: helps Physical server to be able to create multiple VMs

### Virtual servers

ec2 in AWS IAAS

Virtual machine in azure

Compute engine in gcp

### Containers in cloud

Each OS contains a container

Each container will have their own application and their dependency, library, config files

Container will help u create multiple individual application

ECS- elastic container service

## Containers in cloud

Each OS contains a container

Each container will have their own application and their dependency, library, config files

Container will help u create multiple individual application

AWS: ECS- elastic container service

Containers

    Usually smaller microservices

    AWS elastic kubernetes services

    Google: kuberneties

    Azure : azure kuberbetes services

    Each server can create multiple virtual machine using hypervisor

    Each container running in a os can create multiple containerized application within it.

    Benefits of container

    portable

### Fargate:

Takes care of the host, server, compute resources

We will care only about the container and the container image to run our application

## Object vs block storage

### Object

Storing images, files, backups

S3 bucket aws

Azure blob azure

Google cloud storage

Static webpage can be used

Html

Script media

Images

Videos

Here we are not using server and going serverless

And here we are using s3 object to serve the html files

Object storage is a data lake

The size of the object can be of any size

Unstructured data

Block storage

Storing volumes

## Cloud Security

Shared responsibility

My responsibility

Information and data

Devices

Accounts, identities

Cloud provider

Physical host, network, datacenter

    CDN

    Can setup fire wall rules

    Can setup load balancer

    Request comes through cdn

    Aws -- cloudfront

    Gcp -- google cdn

## Databases in the cloud

### Relational databases

Rdbms: sql, oracle,mysql can be run on an unmanaged virtual server(ec2, compute engine)

We have the control

Managed relational databases (RDS, cloud sql, azure sql)

Will be managed by the cloud provider

Control will be less

### Non relational databases

Aws- dynamo db

Gcp: cloud bigtable

Azure: cosmos

With data warehouse it’s a structured data

Large amount historical data

Massively scalable

## Serverless

EC2 - unmanaged instances

Services offered by aws

Lambda - lambda is tiggered and a piece of code is executed

# AZURE

1. cloud concepts

### cloud computing

Ability to rent computing resources

    1. windows and linux servers
    2. unlimited file storage
    3. Databases
    4. Message queues
    5. content delivery network
    6. batch processing jobs

Shared responsibility Model

cloud virtual machine responsibility

    user
    1. operating system patches
    2. network and firewall settings
    3. application settings
    4. authentication settings
    5. authentication plaform
    6. user accounts
    7. devices
    8. data

    Azure
    1. building security
    2. physical network security
    3. physical computer security

cloud app service responsibility

    user

    1. user accounts
    2. devices
    3. data

    Azure
    1. operating system patches
    2. building security
    3. physical network security
    4. physical computer security

    shared
    1. network and firewall settings
    2. application settings
    3. authentication settings
    4. authentication plaform


cloud Saas responsibility

    user

    1. user accounts
    2. devices
    3. data

    Azure
    1. operating system patches
    2. building security
    3. physical network security
    4. physical computer security
    5. network and firewall settings
    6. application settings

    shared
   
    1. authentication plaform

2. azure architecture and services

3. azure management and governane
