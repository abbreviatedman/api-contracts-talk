<!-- splash-page -->

# API Contracts

## An API-First Approach

---

## The Problem

APIs are challenging to build, costly to support, and resistant to change.

At the same time, data is increasingly central to business strategy.

---

## The Solution

In the early stages of API design, spend time on and emphasize:

- hearing from all stakeholders
- comprehensibility for non-technical team members
- designing for adaptability—these early designs should be changeable!
- the API's needs (over the technical details)

---

## What Is "API-First"?

An API-First design focuses on making sure a contract is carefully thought through and drawn up before a single line of code is written.

---

## Why A Contract?

APIs are increasingly looked at as a **business product**, and a **relationship-builder** between:

- an API provider and its API clients
- API developers and sales

It makes sense to write up a contract before these parties do business with each other!

---

## Contract as Documentation

The contract can also serve as human-readable documentation for non-technical team members.

And with the right tools, it can even be turned into web-based documentation!

See SwaggerHub ( https://swagger.io/tools/swaggerhub/) for a great example!

---

## Integration-First

This is the old way of doing things.

1. The API developer team (the "backend") gets the business requirements for the API builds out the first version.
2. The frontend team begins to integrate the API into their app, and provides feedback on changes they need to see.
3. The backend team changes the API to match the request.
4. Repeat steps 2-3 until all requirements are met.

---

## Steps for API-First

1. Identify the project objectives.
2. Understand the data shape needed.
3. Define integration points, i.e., endpoints.
4. Look at what capabilities are needed for the system to function given its environment.
5. Design and implement the API itself.
6. Implement the frontend and backend.

---

## A Note On Terms

**API-First** can be naively interpreted as "the API comes first", when, in fact, the API is finished first with an **Integration-First** approach..

The "first" isn't about **order** but **priority**. API-First prioritizes the _API_ as the most important long-term goal, while Integration-First prioritizes getting it _integrated_ into the more prioritized overall system as soon as possible.

---

## Advantages Of Integration-First

- The API gets up-and-running more quickly.
- Less communication is required outside the technical teams.

---

## Advantages Of The API-First Approach

- The API development avoids later delays in re-working it.
- Fewer changes need to happen when the API reaches its users. 

---

## What A Contract Looks Like

Contracts are often written in a data format called YAML.

(You can use JSON, but YAML is more human-readable.)

Here is one for a straightforward pets API.

https://github.com/OAI/OpenAPI-Specification/blob/main/examples/v3.0/petstore.yaml

---

## Exercises

Let's get out hands dirty!

---

### Exercise 1 - Identifying Elements Of An API Contract

Let's spend 20 minutes seeing if we can identify the parts of this contract.

- What is its base url?
- Does it have an API prefix?
- What is the API's version?
- What endpoints does it have?
- What HTTP verbs does each endpoint have?
- What is the "shape" of the data, i.e., what attributes does a pet have?

---

### Solution 1

- The base url is `http://petstore.swagger.io/v1`
- It does _not_ have an API prefix, using a `swagger.io` sub-domain to mark the URL as an API one.
- The version is 1.
- The endpoints are `/pets` and `/pets/{petId}`.
- The HTTP verbs for `/pets` are GET and POST. Only GET is used for `/pets/{petId}`.
- A Pet object has two attributes: `id` and `name`.

---

### Exercise 2: Writing A Contract

We'll spend 45 minutes writing out a contract in YAML.

---

#### Directions

1. Have someone create a YAML file. Creating a file that ends with `.yaml` should do it!
2. Use the contract pattern from the example to define the following **endpoints**:
  - Get all hotels.
  - Create a new hotel.
  - Get a hotel with the specified `id`.
  - Get the pets that are currently staying in a specific hotel.
3. Use the contract pattern from the example to define the following **data shape**. A hotel should have a
  - `name`
  - `location` ( city name)
  - `pet-type` (e.g., "cat" or "dog" or "rabbit")
4. If you have time, come up with a data shape for a pet!
  
---

#### Tips

- Use your best judgement on what looks like an important element you should define first.
    - For example, `summary` is where the description goes, and that's something we've included in the past.
- Only then define attributes we haven't covered, if you have time _after the whole exercise is complete_, like:
  - `operationId`
  - `type` for properties
- YAML requires two spaces for each level of indentation.
- ... but we're not writing production code here, so _don't_ sweat the syntax!

---

### Solution 2

Hosted here:

---

<!-- splash-page -->

# The API Lifecycle Is Complete

### Cue "The Circle Of Life" from The Lion King!



