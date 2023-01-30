Developer know what can be done to implement

Architect know what should be done

### Responsibility:

Fast, secure, reliable, maintainable, scalable

Role: no manager work

Architect should code, can gain trust from developers

Trust worthiness

Support developers

respect

### Certification:

TOGAF

## Types of architect

### Infrastructure architect

    Design about servers, vm, storage

### Solution architect

### Enterprise architect

    Doesn’t have to be technical, if technical its a plus , talk with senior management

## Architect mindset

Need to know the business

How is the company doing business wise

Read about the company

Deep understanding of the business

What is the growth strategy

What is it weakness

Who is the competition

Founders, revenue

line of products

Whether the companty publicly traded

What keeps the ceo awake night

How the systems are integrated

You need to think about the end users who is going to use it.

### Watch your language

Always keep in mind what is the thing that really matters to the person you are talking to

How to talk to different people in company

To team leader : we need to say we will use the latest version of the react , we can use functional components

To CEO: we have designed a system which will handle the sales of the black friday

To Manager: we are going to use a framework which help to reduce to write less code which will help in budget funding

## System or functional requirements

What the system has to do

Business flows (login,)

Business services

User interfaces

## Non functional requirements:

No of users

Volume

How much data the system will accommodate over time

Day 1 500mb, annually 2 tb

Load

Quantity of work without crashing

Availability of the system

How much users it can handle without crashing

Performance

Always talk in numbers

Need to find out the numbers(is it 5 mins or 10 secs or 700 millseconds)

### Latency

How much time the service takes to push the data to datastore or back to user

### Throughput

How many task can be performed in given amount of time

### Concurrent users

How many users using the application simulataneously

### SLA

Required uptime of the system

Need to discuss about the system uptime.

Accessibility

### Scalability:

adding computing resources without any interruption

Scale up

single big machine

Can crash

Scale out

Multiple system

Redundancy so one crash other system will support

So no limit can add many as we need

Add vm and notify load balancer

### Managebility

Report status and problems by monitoring

### Modularity

Make code in separate entity so that we deploy independently one module if any issue occurs or want to depploy separately

### Extensibility:

Extend the code and not by modifying the code

### Testability

Manual

Unit testing

small unit

Independability

Single responsibility

Integration testing

To deal 600 MB of data(for pdf upload size of the pdf can differ, so that should not lag the user experience)

Client don’t know about these non functional requirement

Much more important than the regular requirements

## Map the components

Understand the system functionality

Communicate with the client regarding the functionality so there is no gap

## Select the technology stack

Frontend

React vs Angular

Datastore

SQL

relational database

stores data in tables

SQL sql query language

When? Not huge and when data is structured

NOSQL

For scale and performance(storage of data)

Schema less

Data usually stored in json format

When ? Data is huge and not structured

Made with clear mind

Discuss with the team members

Irreversible

Check in google trends(popularity)

Cross platform ?

Backend

Python

Cross platform

Easy to learn

Dynamic type system ?

Mobile app:

Native apps:

Hybrid

Cross platform

## Design the architecture

Caching

Discuss with the team so you get inputs from the team if you have not known about the areas which they knew

## Write the architecture document

Write the architecture and share it with the management and the developers

Support the team

Architecture will be changed so need to support the developers

## Different application types

Web apps

Browsers send http request to web servers(request & response model)

Web api

Usually rest based api (http verbs)

Returns data not html

Request and response based model

Mobile

Usually works with web api

Console

No fancy ui

Required technical knowledge

Long running process

Service

No ui at all

Desktop

Has all its resources on the pC

Eg word, gaming apps

## Component architecture

Do not distance yourself from code

Don’t use new classname() // its bad

That’s when we use interface ? Dig more

Rather use dependency injection to get the instance of the object

Dependency injection makes the code more modular , easy to maintain

### Naming convention

Lower camel case carEngine -Javascript

car_engine -python

### Exception Handling

Catch the specific exception so that you find the right exception and show corresponding error to user

### Logging

Logging is very important to track errors and investigate

Gather data

Where we can store the logs files, database, event log(kibana)?

## Design patterns

Reusable solutions to common problems

Make your code readable

Solutions Tested and used by other developers

### Factory pattern

Creating object without specifying the exact class of the object.
Avoid strong coupling between classes
New is glue

### Repository pattern

Share similarities with data access layer

### Façade pattern

Creating a layer of abstraction to do some complex action

### Command pattern

All the actions information is encapsulated in a object

## System architecture

How will system work under heavy load?

What will happen if the system crash at this exact moment in the business flow

Loose coupling

Stateless

Application state is stored in datastore and user interface

Load balance distributes load to different services

Caching

Server gets data server initially and then it gets data from cache instead of the server

Its faster to retrieve

Cache should hold data that is frequently accessed and rarely modified

Inmemory inprocess cache

Distributed cache

Messaging

Means of communication between various services

Messaging types

a) Rest api
for python flask

b) Http push notification

Client subscribe to event and if an event occurs it notifies the server

Eg Web sockets

Client notify the server

c) Queue
message will be handled once and only once

Messages will be handled in order

d) file based and database based

Logging & monitoring

Monitoring : shows the current health status
