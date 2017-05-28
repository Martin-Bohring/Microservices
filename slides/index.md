- title : Microservices
- description : Oportunities and challenges implementing Microservice Architectures
- author : Martin Bohring
- theme : night
- transition : default

***
- id : title

### Oportunities and challenges implementing Microservice Architectures ###

Martin Bohring 2017

***
- id : history

### A little bit of history ###

on distributed systems and programming styles

***
- id : history90Approach

#### The 90's approach ####

- Heavyweight *RPC* based systems based on *IDL* (Interface Desciption Language) lifted from the 80´s
- Heavyweight distributed object systems like *CORBA* and *DCOM* and others also based on *IDL* dialects
- Code generation based on *IDL*

***
- id : history90Outcome

#### The 90's outcome ####

- The code generation caused the following:

  - Strong coupling betwen services and clients
  - Vendor lock in through libraries and runtimes
  - Big up front costs and slow rollouts
  - A lot of coordination between teams and companies

**Result:** Distributed developer hell

***
- id : history2000Approach

#### The 2000's approach ####

- This time we do better
- Let´s stay programming language agnostic
- Lets´s get rid of *IDL*
- Let's be Internet ready and build on *HTTP* and *XML*
- So *SOAP* (Simple Object Access Protocol) was invented and used *POST* for calls and reads

***
- id : history2000Outcome

#### The 2000's outcome ####

- But that was not sufficient or enterprice ready

  - So a description language (*WSDL*) was invented
  - A way to relate calls to each other was invented (*WS-Adressing*)
  - A way to deliver events was needed (*WS-Eventing*)
  - Service address hardcoding was a pain, so service discovery was created (*WS-Discovery*)
  
**Result:** Distributed developer hell (XML edition)

***
- id : history2010Approach

#### The 2010's approach ####

- They got it all wrong in the past
- We need loose coupling and not *RPC* style communication
- *XML* is to heavyweight, so let's use *JSON* instead and keep *HTTP*
- Let's leverage the Internet architecture and use *POST* for writes and *Get* for reads
- Lets base architecture and communication on hypermedia (*HATEOAS*)
- Lets not be statefull within our services but let the client transfer the state.
- So *REST* as an architecture style was invented.

***
- id : history2010Outcome

#### The 2010's outcome ####

- It started lean and mean, but some well known patterns showed up

  - We need events and subscriptions and so *WebSocket* was invented
  - A formal *API* description was needed and so *Swagger* and *RAML* where invented
  - *POST* vs *PUT* vs *PATCH* wars arose, so rules when to use what had to be established
  - We need to secure our *API*, so *JWT*, *OAuth*, *OAuth2* and other token based approaches where invented
  
**Result:** Distributed developer hell (JSON edition)

***
