# Building the first product

## Summary

Getting a first software product to market quickly depends more on decisions than on coding speed. Nine principles help: know the real goal of the first version, cut the scope hard, trust the product team, focus on delivering value, decide fast, keep business and technology talking to each other, teach stakeholders the process, choose the technology stack for speed and stability, and make technical choices for business reasons. Together they can shorten a first release from months to weeks.

## Prerequisites

- [Minimum viable product](minimum-viable-product.md)

## Core concepts

### Definition

*Building the first product* means turning a validated idea into a working version that real users or investors can use, under tight limits of time and money. The principles below are practitioner guidance from agile software development and product management (see Cagan, 2017, and the Scrum Guide). A *product owner* is the person responsible for maximizing the value of the product, mainly by deciding and ordering the *backlog*, the list of work still to do.

### Analogy

Building a first product is like packing for a short trip with only hand luggage: you decide what the trip is for, take only what serves it, and buy the rest on arrival. Packing for every possible event means checked bags, delays and lost luggage. The analogy breaks because in software you can add things later at low cost only if the foundations were chosen well.

### Mechanism

1. **Focus on your real goal.** Decide what the first version must achieve: a prototype for investors, an MVP for real customers, the optimization of a business process, or something else. The goal decides what "done" means.
2. **Reduce the scope.** Cut the backlog to the absolute minimum, ideally with an experienced product owner. Practitioners claim this can save most of the development time; the size of the saving depends on how bloated the starting scope was.
3. **Trust the product team.** Shorten decision-making by giving part of your responsibility to the product owners and the developers.
4. **Focus on value delivery.** For a stable pace, let the development team balance quality, functionality and speed. Fixing all three from outside produces overtime or hidden shortcuts (*technical debt*: shortcuts that make later changes slower).
5. **Make tough decisions fast.** Do not fear a wrong decision. Hesitation often costs more than reworking a piece of software.
6. **Communicate within and outside the team.** The product team needs business context, and the business needs to understand the technology.
7. **Educate stakeholders about the development process.** Software products rarely have a single owner. Make sure everyone involved knows and follows the process, so that the team is not pulled in several directions.
8. **Choose the technology stack wisely.** Save months by integrating third-party software-as-a-service providers (payments, authentication, email), reusing existing components and deploying on stable infrastructure that needs little maintenance.
9. **Mitigate technological risk with business-oriented decisions.** Every technical novelty must serve a business goal. Explore new technologies when the business needs them, and build with well-known, proven frameworks.

The principles group into three concerns: what to build, how the team works, and what to build it with.

```mermaid
flowchart LR
  subgraph What
    G[Real goal] --> SC[Reduce scope]
  end
  subgraph How
    T[Trust the team] --> V[Value delivery]
    V --> D[Decide fast]
    D --> CM[Communicate]
    CM --> E[Educate stakeholders]
  end
  subgraph With
    ST[Wise stack] --> R[Business-led tech choices]
  end
  SC --> T
  E --> ST
```

## Worked example

A logistics company wants an app for drivers to confirm deliveries. The first plan has 60 backlog items, including route optimization, chat and a rewards system, with an estimate of nine months.

- **Goal:** replace paper delivery slips in one depot, measured by fewer lost slips and faster invoicing.
- **Scope:** the product owner keeps eight items: login, list of today's deliveries, photo of signature, offline mode, sync, export for invoicing, basic admin and error reporting.
- **Stack:** a cross-platform mobile framework the team already knows, a hosted authentication service and a managed database.
- **Decisions:** the operations director gives the product owner the right to decide on scope within the goal, and meets the team once a week instead of approving each change.

The first depot uses the app after ten weeks. Route optimization is reconsidered only after three months of data. The numbers are invented for the example.

## Trade offs and when to use it

Speed now can create technical debt that slows later work, and relying on third-party services creates dependency and running costs. These trade-offs are usually worth it for a first version, because the biggest risk is building the wrong thing. Once the product proves itself, budget time to repay technical debt and to review vendor choices.

## Common mistakes

- **Starting without a stated goal for the first version.** Write one sentence: who will use it, for what, and how success is measured.
- **Several stakeholders changing priorities directly with developers.** Route all priorities through one product owner and a shared process.
- **Choosing a new technology because it is interesting.** Choose proven tools unless a business need requires something new.
- **Waiting for certainty before deciding.** Set a deadline for each decision and accept that some will be reworked.

## Practice

1. What is a product owner responsible for?
2. Why should the development team balance quality, functionality and speed itself?
3. Give two ways to save months when choosing a technology stack.

### Answers

1. Maximizing the value of the product, mainly by deciding and ordering the backlog.
2. Because fixing all three from outside leads to overtime or hidden shortcuts that slow later work.
3. Use third-party services for common functions (payments, authentication) and reuse existing components on stable, low-maintenance infrastructure.

## Further reading

- Cagan, M. (2017). *Inspired: How to Create Tech Products Customers Love (2nd ed.)*. Wiley. Product management practice.
- Schwaber, K., Sutherland, J. (2020). The Scrum Guide. [Link](https://scrumguides.org/scrum-guide.html). Definitions of product owner, backlog and the team process.
