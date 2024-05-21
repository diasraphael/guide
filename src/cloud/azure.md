# AZURE

Before cloud we need to buy a server, install it,maintain it,replace it,have an it team to manage it.

1. cloud concepts

### cloud computing

Ability to rent computing resources

    1. windows and linux servers
    2. unlimited file storage
    3. Databases
    4. Message queues
    5. content delivery network
    6. batch processing jobs

- compute, networking, storage and other services managed by someone else.
- if u need a server u can create in minutes
- pay as what you use
- shut it down when not needed.
- automatically maintained, patched,secured, monitored

### Cloud characteristics

1. on demand self service(no human interaction, available 24/7)
2. broad network access(can be accessed from anywhere using the network, no physical access)
3. resource pooling(resources are shared between customers)
4. rapid elasticity(resources can be scaled up and down automatically)
5. measured service(payment is done only for resources actually used)

### Capex vs Opex

1. Capex: investment for the future, not flexible
2. Opex:pay as per wish, flexible

### Iaas

1. cloud provides underling platform (compute,network,storage, virtualisation,networking managed by cloud) eg virtual machine(install software,patches it, maintains it)

### Paas

1.eg webapps, need to develop application and deploy code

### Saas

1. running completely in cloud(office 365)

## Regions

1. datacenter location is called as regions
2. azure has 60 regions
3. almost every resource we use need to be put in a region(check if the service is available in that region)
4. cost diff between different regions

## Zone

1. some of the regions may have one or more physical datacenter
2. availability, if one failed, availability zone is free
3. when there are more than one datacenter in a region, the region is said to have availability zones
4. load balancer knows whether the vm is down or not so that it redirects the request to the machine which is active

## paired region

1. when one region is completely failed then the paired region will help to support the application
2. this is set by azure, so that when data is set in one region and is failed.

## Account && Subscription

1. Account: an identity with access to resources in the subscription(can be attached to lot of subscriptions)
2. subscription: contains the various resources you provision in the cloud(can be attached to lot of accounts)
3. once u create an account a subscription is attached to the account(identity) automatically by azure.
4. cost associated with an account

## Resource group

1. it is a container that holds related resources for an azure solution and that will attached to a subscription.creating a resource group is free.
2. we can create a resource group via portal or via azure cli(bash or powershell)
3. it is used for grouping resources(dev group, prod group, test group)

## Storage

1. can be used to store something in azure
2. quite cheap

## SLA

1. always check the SLA for the services used.(SLA for the app service used)
2. sla calculator: https://uptime.is/
3. azure calculator to find the pricing of the services
4. linux is more cheaper than windows
5. 154 dollars for a month for a VM => windows

## Cost Management & budget

1. cost management for billing
2. create budget

## Compute

set of cloud services for hosting and running applications. allows uploading your code and then running it. four types of compute services are

1. virtual machines :virtual(not real) server running on a physical(real) server. its a regular server and can connect using RDP protocol.unmanaged service.we connect windows machine using RDP. linux machines using ssh.

   - select the location
   - select the image
   - select the size(dont forget to check the price)
   - cost of the vm includes vm, disk, ip, storage=approx total 180 dollars
   - check price of nearby regions
   - select linux over windows

2. App services

   - A fully managed hosting for websites
   - publish your code and it runs
   - integrates with many source control and devops engines(github, azure devops, bitbucket,dockerhub)
   - supported platforms(nodejs,python)
   - supports containers
   - app types: web apps,web api, web jobs(batch process)
   - there is azure extension to deploy our app
   - 73usd/month(estimated or approx) need to check the nok value
   - By default, App Services can be accessed using http and https. You can make it https only in the TLS/SSL settings in the App Service menu.
   - With VM - you pay only when the VM is On.
   - With App Service - The only way to stop paying for it is to completely delete it.

3. AKS

   - azure kubernetes services: most popular container management platform.
   - provides all aspects of management: routing,scaling,high availability, automated deployment,configuration
   - allows deploying containers and managing them using kubernetes services.
   - containers: thin packaging model packages software, its dependencies and configuration files
   - can be copied between machines

   containers vs virtual machine

   - containers uses the host operating system to run the software instead in vm, on top of hypervisor we can install any no of vms and inside the vm we will have their own guest operating system and on top of that we will have our own software to run.
   - containers can start up very fast in seconds
   - u can have many no of containers in the server but can have very limited no of vms

   Docker: is the container environment.

   - dockerfile contains instructions for building custom images.
   - docker daemon or docker server => builds images
   - images are static files contains the software to run

   Container Management:when there is a lot of containers.

4. Azure functions

## ARM template

1. it is json file based on which resources are created.

## virtual machine scale set

1. VMS can be scaled out manually and automatically

## Deploying an application to azure

1. azure account extension used for authentication purpose when we try to use some azure commands.
2. azure app services extension is available check what all we can do with that
