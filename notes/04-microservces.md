[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Microservices

### Software as a Service (SaaS)

Is a model that implies that your software product is:

- Available 24/7
- Scales elastically
- Is highly available and fault-tolerant
- Provides a responsive user-experience on all popular devices
- Does not require the user to install a client, perform updates or patches
- And the software product is always the most recent and up-to-date version (and is deployed and maintained using a process called _Continuous Delivery_)

### Continuous Delivery

Is a process defined by the following capabilities:

- The software is developed in a high-velocity, iterative approach and is deployable throughout its lifecycle
- Deployment to development, test, staging and production is managed using an on-demand automated process
- If there is ever any issue with the deployment process, fixing it takes priority over delivering new features

### Lean Engineering

“Build → Measure → Learn → Repeat.”

- Is a high-velocity product development approach that builds on _Agile_ and _Scrum_ to include deployment into production
- Testing, surveying and feedback-gathering from customers is key as any new learnings is then folded into the next development iteration
- Lean Engineering (also called _Build-Measure-Learn_) promotes Continuous Devliery, Continuous Analytics and Continuous Feedback

### DevOps

- Development Processes need to be automated (as much as possible) in order to support Lean Engineering/Continuous Delivery
- This is called **DevOps** and it is both a culture and a set of tools & tech used for automation
- Culturally, it can be most challenging to organisation as it implies that teams need to be organised in mixed groups of developers, architects, quality assurance and operations

## Microservices

A **microservice** is a software building block that does _one thing and does it well_. The goal of a microservice is such that:

- It is highly scalable
- Provides fault-tolerance
- When it is no longer needed, can be de-provisioned

### The Benefits of Microservices

- ✅ Evolutionary
- ✅ Open
- ✅ High Velocity
- ✅ Reusable and Composable
- ✅ Flexible
- ✅ Even a single team can be solely responsible

### The Challenges of Microservices

- ⚠️ Organisation (e.g. which teams are responsible for what microservices?)
- ⚠️ Platform (e.g. where and how should they run? Which platforms enable more communication and which are too excessive?)
- ⚠️ Identification (e.g. how refined should tasks be split into microservices?)

### Microservice Architecture

- **SDK Layer** — a library, tool or service that allows faciliates development of an app and defines the language specific to a microservice (e.g. NodeJS and Javascript)
- **API Gateway Layer** — a system that routes requests to a specific service that will handle it (e.g. ExpressJS)
- **Protocol Layer** — the communication mechanism (e.g. REST HTTPS)
- **Service Layer** — where the actual work happens (e.g. index.js)
- **Data Access Layer** — responsible for the communication between services and where data is stored (e.g. firebase-communicator.js)
- **Store** — where data can be stored (e.g. Firebase)
- **Automation** — tools that facilitate the development and deployment of each microservice (e.g. CodeShip, BuildKite, etc.)

### Microservices vs Monoliths

Traditionally, apps are built as giant monoliths composed of a stack of giant codebases:

| Product |
| :---: |
| UI |
| Business Layer |
| Data-Access Layer |
| Database |

Apps built out of microservices, on the other hand, are composed of small connected codebases — each with their own _specific functionality_:

| Product 1 | Product 2 | ... |
| :---: | :---: | :---: |
| Microservice | Microservice | ... |
| Microservice | Microservice | ... |
| Microservice | Microservice | ... |
| Microservice | Microservice | ... |
| Database 1 | Database 2 | ... |

As a result, microservices can be enginered to: 

- Run _autonomously_ (i.e independent of other microservices)
- Run _isolated_ (i.e. running on a different deployment scheme, etc.)
- Be _elastic_ (i.e. can be expanded or shrunk depending on usage demand)
- Be _resilient_ (i.e. can easily be fixed should something bad happen)
- Be _responsive_ (i.e. quick to respond or react)
- Be _configurable_ (i.e. built to only serve a highly-specific purpose)

#### An Example

Consider an eCommerce app currently built as a monolith: a singular codebase responsible for:

- Displaying the front-end interface
- Calculating and handling sales and transactions
- Communicating with the database (in terms of user accounts, purchases, and stock available)

The eCommerce app can instead be re-built as a stack of microservices:

- An remote app that displays the front-end interface, which communicates to
- A server that calculates and handles sales and transactions, which also communicates with
- Another server that manages the database

The above services can be further split into smaller microservices, such as for example:

- A piece of software within the server responsible for calculating sales
- Another piece of software within the server responsible for business transactions
- A piece of software the only manages the user database
- Another piece of software that only manages the stock database
- And so on...

## REST Architecture

- **REpresentational State Transfer** is a web-standards-based architecture that uses HTTP
- Involves requesting and returning resources accessed via HTTP standard methods
- A **REST Server** provides access to resources
- A **REST Client** access and modifies resource by communicating with the REST Server using HTTP
