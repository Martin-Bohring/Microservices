- title : Distributed Architectures
- description : Oportunities and challenges implementing distributed architectures
- author : Martin Bohring
- theme : night
- transition : default

***

- id : title

### Oportunities and challenges implementing distributed architectures ###

Martin Bohring
<br />
2017

***

- id : intro1

#### Every distributed system architecture has to answer the following questions ####

- How are commands executed?
- How to perform queries?
- How to publish events?

***

- id : intro2

#### And in addition ####

- Do we need to scale?
- How do we scale?
- Is a *CRUD* (Create, Read, Update, Delete) approach sufficient?
- How to deal with flaky connections?
- How to deal with latency?
- How to handle idempotency?
- How to address asynchronity?
- Do we need to handle security on all endpoints?
- ...

***

- id : history

#### A little bit of history ####

on past approaches to answer those questions over the last 3 decades

***

- id : history90Approach

#### The 90's approach ####

- Heavyweight *RPC* based systems based on *IDL* (Interface Desciption Language) lifted from the 80´s
- Distributed object systems like *CORBA* and *DCOM* and others also based on *IDL* dialects
- Code generation based on *IDL*

***

- id : history90Outcome

#### The 90's outcome ####

- Strong coupling betwen services and clients
- Vendor lock in through libraries and runtimes
- Big up front costs and slow rollouts
- A lot of coordination between teams and companies
- Asynchronous handling was only an afterthought
- Chatty message exchanges that broke down on network outages

**Result:** Distributed developer hell

***

- id : history2000Approach

#### The 2000's approach ####

- This time we do better
- Let's stay programming language agnostic
- Let's get rid of *IDL*
- Let's be Internet ready and build on *HTTP* and *XML*
- So *SOAP* (Simple Object Access Protocol) was invented and used *POST* for commands and queries

***

- id : history2000Outcome

#### The 2000's outcome ####

- A description language (*WSDL*) was needed
- A way to relate calls to each other was invented (*WS-Addressing*)
- A way to deliver events was needed (*WS-Eventing*)
- Service address hardcoding was a pain, so service discovery was created (*WS-Discovery*)
- Endpoint and message security was required, so another standard was created ("*WS-Security*")
- The support of that standard family (*WS-..*) was different depending on the programming ecosystem of choice

**Result:** Distributed developer hell (XML edition)

***

- id : history2010Approach

#### The 2010's approach ####

- They got it all wrong in the past
- We need loose coupling and not *RPC* style communication
- *XML* is to heavyweight, so let's use *JSON* instead and keep *HTTP*
- Let's leverage the Internet architecture and use *POST* for commands and *Get* for queries and *PUT* for updates
- Let's base architecture and communication on hypermedia (*HATEOAS*)
- Let's not be statefull within our services, but let the client transfer the state.
- So *REST* as an architecture style was born (<http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm>).

***

- id : history2010Outcome

#### The 2010's outcome ####

It all started lean and mean, but then some well known patterns showed up

- We need events and subscriptions and so *WebSocket* was invented
- A formal *API* description was needed and so *Swagger* and *RAML* where created
- *POST* vs *PUT* vs *PATCH* wars arose, so rules when to use what had to be established
- We need to secure our *API*, so *JWT*, *OAuth*, *OAuth2* and other token based approaches where invented

**Result:** Distributed developer hell (JSON edition)

***
