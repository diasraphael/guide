## Software Architecture

1. everything has an architecture whether we think or not think about it
2. it is important to consider when we start, the more we invest it is harder to change the structure.
3. many ways to organise our code
4. it impacts the performance and scale of the product, ease of adding new features, response to failures.

### definition

the software architecture of a system is a high level description of the system's structure, its different components and how those components communicate with each other to fullfill the systems requirements and constraints

1. this means technologies or programming languages are not a part of the software architecture but a part of implementation.
2. decision of choosing the technologies must be at the very end of the design.
3. the components should do what the system requirement is and should not do what the system requirement is not
4. not doing a good job at the design phase can waste months of engineering time.
5. restructuring a system that was not architected correctly is very hard and expensive.
6. the stakes here are high.

### software development life cycle

design (software architecture)-implementation-testing -deployment

### system design or interviews

system design has high level of ambiguity

1. reason being the person providing the requirements are not very technical
2. gathering the requirements is part of our solution
3. the client doesnt always know what they need
4. the client generally knows what the problem they need to solve.

eg:allow people to join drivers on a route who are willing to take passengers for a fee.

clarifying questions

1. real time vs advanced reservation
2. user experience - mobile or desktop
3. payment directly or payment through us

### what happens if we dont get the requirements right?

1. what happens if we dont get the requirements right?
2. we can simply build something and fix it.
3. seemingly there is no cost of materials in software so chnages should be cheap.
4. large scale systems are big projects that cannot be easily changed
5. many engineers are involved.
6. many months of engineering work.
7. hardware and software cost
8. contracts include financial obligations
9. reputation and brand will be lost

### gathering requirements

1. ask the client to describe everything they need
2. most powerful method of gathering system requirements is usecases,userflows(sequence diagram)
3. sequence diagram: Diagram that represents interactions between actors and objects.(entities)
4. its a part of unified modelling language(UML). standard for visualizing system design.
5. UML diagrams are used mostly for system design. no real standard diagrams representing software architecture in industry
