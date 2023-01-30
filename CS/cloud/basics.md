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
