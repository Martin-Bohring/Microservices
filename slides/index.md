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

***
- id : history90

#### The 90's approach ####

- Heavyweight RPC based systems based on IDL (Interface Desciption Language) lifted from the 80´s
- Heavyweight distributed object systems like CORBA and DCOM and others also based on IDL dialects

  - leading to strong coupling
  - leading to vendor lock in
  - and big up front costs
  - and a lot of coordination between teams and companies

**Result:** Distributed developer hell

***
- id : history2000

#### The 2000's approach ####

- This time we do better
- Let´s use human readable XML for everthing and let´s stay programming language agnostic
- Lets´s get rid of IDL
- So SOAP (Simple Object Access Protocol) was invented
- It is still about distributed objects, but this time based on XML and HTML

- but that was not sufficient

  - so a description language (WSDL) was invented
  - A way to relate calls to each other was invented (WS-Adressing)
  - A way to deliver events was needed (WS-Eventing)
  - Service address hardcoding was a pain, so service discovery was created (WS-Doscovery)i

**Result:** Distributed developer hell XML edition

***
