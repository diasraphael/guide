# Cloud

On demand network access to a shared pool of configurable network resources(eg, networks,servers,storage,application and services)that can be rapidly provisioned and released with minimal management effort or service provider interaction.

### cloud model has 5 characteristics

1. on demand self services: allowing computing users to manage their own resources without interaction with a service provider.
2. broad network access
3. resource pooling
4. rapid elasticity
5. measured service utility

### cloud model has 3 service models

1. IAAS
2. PAAS
3. SAAS

### cloud model has 3 deployment models

1. private cloud
2. public cloud
3. hybrid cloud

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
