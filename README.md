# Proposal: %loam — Golem + Urbit Dev Suite Grab Bag

## Elevator Pitch
In order to terraform mars, urbit will need a rich soil to grow its software both from urth and mars. In other words, it needs %loam — a loosely-coupled set of opinionated standards and dev tools that connect the existing software and tooling into a cohesive and consistent model, so that apps being built in different parts of the terrain are more inter-navigable, and interoperable.

# Overview

## Purpose

The loam proposal is slightly non-standard. Rather than proposing a single specific piece of software with sequential milestones, this document describes a "grab bag" of useful developer tools that can be built in any order or even in parallel. We are consolidating them here for ease of review, as well as to show how they are loosely united under a common initiative. 

The main goals of these standards and tools are to make Urbit development more:
1. **Cohesive** — It should be easy and painless to have all of the state-of-the art dev tools in your Ubrit projects out of the box, and working together
2. **Consistent** — Piping between dev tools should be consistent across different projects, it should be effortless to implement best practices when starting your projects, so that devs from other projects can open it up and immediately understand what is going on

## Scope

Here is a shortlist of things that need to be solved for this goal:

* Project Creation 
* Code Scaffolding for Hoon
* An opinionated framework for Hoon
* Binary Management
* Package/Dependency Management
* Standardized Deployment Pipeline
* Urth-side livereload
* Urth -> Mars Message passing
* IAC (Infrastructure as Code) For Dev Envs
* A drop-in solution for NoSQL Data 
* DID Resolution

You should be able to take advantage of these things — \
— whether you are developing in mars or urth, \
— whether you are building in javascript or hoon or a mixture of the two, and \
— whether you are building a generator, agent, or webapp. 

This allows for flexibility where it is important to devs while providing opinions and standards for the things that get overlooked and take up development time when creating new projects and companies. 

![CYOA](./img/CYOA.png)

In order to facilitate this, there are a few different things that need to be built:
1. **CLI (golem)** — and urth-side CLI for project creation, scaffolding, and binary & dependency management
2. **Dojo Tool/IDE** — a desk of threads and opinionated pill for project creation, scaffolding, and binary & dependency management in mars. 
3. **clack** — a js wrapper around conn.c to make your fakeships scriptable from JS on MacOS
4. **BaaS** — a desk for a NoSQL Store that can be used as a BaaS, allowing JS-first developers to move business logic to the frontend
5. **Package Manager** — an urbit instance of an [Egyn]() registry for managing packages, binaries, and other urbit artefacts
6. **DID Resolver** — <what actaully is this>
7. **Curation Mechanism**  — a curation UI for browsing packages, binaries, and other urbit artefacts

In addition, there are some integrations that don't fit neatly into one of these projects, included in this document as well. 

The Second part of this proposal doc will go into each of these in more detail. First we will paint a 500 ft view of how these fit together into a consistent workflow.

## Workflow

The goal of providing these tools is to free up developer time and creativity from reimplementing the piping between layers of an app all the time, as well as to standardize key steps in the SDLC for urbit so that primitives being built and shared loosely conform to legible conventions. Namely, it should be trivial to create, compose, test, and deploy/publsih an app from your local environment, wether on Urth or Mars.

![CYOA](./img/SDLC.png)

This process can be broken down further for both urth and mars development as seen below:

![CYOA](./img/SDLC-URTH.png)

![CYOA](./img/SDLC-URBIT.png)

These diagrams highlight where the steps of the SDLC require different tooling from different environments, while still preserving the ability to have one set of best practices and project structure within a given app. 

Here is a 500 Foot view of how the these fit together from end to end:

![CYOA](./img/500-foot.png)

# Design and implementation

## clack — Design

* Segments
* Stories
* Engineering Design
* UI/UX Design

## golem — Design
    * …

## …

# Milestones (Grab Bag Style)

The loam proposal is slightly non-standard. Rather than proposing a single specific piece of software with sequential milestones, this document describes a "grab bag" of useful developer tools that can be built in any order or even in parallel. We are consolidating them here for ease of review, as well as to show how they are loosely united under a common initiative.

Given that, this list of milestones is not in a strict order but rather a suggested order. We try to note the few strict dependencies where possible

### clack — N Stars

### golem — Project Creation — N Stars
 
* Partially dependant on clack

### golem — Project Scaffolding — N Stars

### Dojo Tool — Creation and Scaffolding — N Stars

### Package Manager — Contracts and Deployment — N Stars

### golem — Binary and Package Management — N Stars

* Dependant on Package Manager.

### Dojo Tool — Binary and Package Management — N Stars

* Dependant on Package Manager.

### golem — Deployment Pipeline — N Stars

### Dojo Tool — Deployment Pipeline — N Stars

### BaaS — data store — N Stars

### BaaS — permissions and replication — N Stars

### DID Resolver — N Stars

### Curation Layer — N Stars

* Dependant on Package Manager.

### Integrations: _____ — N Stars
