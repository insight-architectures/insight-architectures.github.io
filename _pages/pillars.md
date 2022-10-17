---
permalink: /pillars/index.html
title: Our pillars
---

At Insight Architectures, we love facilitating our customers' growth by satisfying their needs for software solutions that help their business.

Because we are tasked with designing and developing parts critical to the business of our customers, we have defined a list of pillars that helps us delivering a product we can be proud of.

## Architecture design

Software development has reached a state where everybody can solve today's problems. On the other hand, a properly designed software architecture can add value not only solving today's problems. Instead, it can sustain the growth of a business by facilitating the addition of new features and the support for future use cases.

By carefully studying the problem at hand, we at Insight Architectures focus on understanding the core use cases and spotting the volatilities of the system.

The core use cases and the volatilities help us design a system that is able to react to changes with agility so that the system will stay aligned to the customer's business.

## Project design

Even the best architecture needs a carefully designed plan to be built. This is even more important when coordinating a team.

By carefully studying the several options available to build the system, project design helps our customers taking informed decisions regarding factors like resource allocation and project duration that inevitably affect the execution of the project. Project design helps uncover and properly handle the compromises between all these factors. With our help and counsel, the customer will be able to choose the project plan that best fits their needs in terms of costs and duration.

Obviously, like everything in software development, a project design isn't set in stone. Delays, redistribution of resources, changed priorities and added features are all but some of the causes that help a project plan evolve over its execution.

Since these changes are continuously tracked, managed and communicated back to the customer, a properly designed and maintained project plan can help keeping track of the advancement of the development and provide accurate estimates on project completion right from the beginning.

## Developer experience

Developing and maintaining any software system, especially if distributed and based on cloud technologies can be extremely burdensome for developers. Starting the several components, each with their own configuration, making sure they all can communicate with each other, while retaining the ability to attach a debugger to any of those components, are all tasks that can take the focus from developers and impact on their ability to provide sensible value to their company.

Having in mind the developer experience while designing the system makes sure that those assigned to develop and maintain the system have all the tools needed to boost their productivity both when developing new features and troubleshooting the system in production.

At Insight Architectures, we believe that a fruitful developer experience can be built around three main approaches.

### Integrating over building

Our customers ask us to deliver them systems that can quickly add value to their business. Most of the times, the value lies in the implementation of the company's business logic not by reinventing the wheel for any engineering task needed to be performed. Delegating these need to existing libraries helps reducing the area of intervention for the developers and, consequentially, freeing up time and mental space for company specific tasks and needs.

Whenever needed, Insight Architectures maintains a set of open source libraries that offer low-level infrastructural helpers that can be integrated in the systems being built for the customers. Our libraries are released with a perpetual MIT license (unless upstream dependencies require otherwise) and can be freely used by our customers. Furthermore, we strive to follow the semantic versioning strict guidelines to help our customers' developer having a clear understanding on whether a new version of these libraries will introduce breaking changes, new features or simply patch previous unintended behaviors.

### Optimized inner development cycle

Being focused on building cloud-based distributed systems, we understand the importance of being able to quickly spin up locally the entire system being built or troubleshooted to be able to test and debug the behavior of the application.

Tools like Microsoft Tye, Docker Compose, LocalStack are all incredible tools available to us to craft a powerful and productive inner development cycle that helps developers adding value to the business with incredible velocity.

### Observability

The final aspect needed to consider for a productive developer experience is observability. Observability is the ability for the maintainers of a system to understand how it is behaving in production without the need to halt its execution.

Techniques like tracing, metrics collection and logging are concerns a system should be designed around from the very beginning. Clear and rich dashboards and carefully defined log filters should be part of the system and not simply an after-thought.

In the latest years, the industry has undertaken an effort to unify the extremely heterogeneous offer in the observability branch. From this collaboration, the Open Telemetry standard is being defined and implemented by all the actors of the many actors in the observability space.

By leveraging the Open Telemetry standard, we can make sure the systems we design and build for our customers are able to integrate with the most popular observability tools.

## Automated testing

In modern software development, automated testing has become paramount for the lifecycle of any application because it helps detecting deviations of the application behavior as soon as possible. Therefore, the meaning of automated testing has evolved from _"proving it's working"_ to _"asserting the expected behavior"_.

Complex software systems are usually covered by a suite of automated tests that is composed by different type of tests.

The most common ones are:

- _Unit tests_ target each individual component of the system, be extremely fast to run and should avoid any kind of interaction with dependencies.
- _Integration tests_ aim to ensure that all components are able to integrate and properly perform their role in the overall application. These tests usually target mocked versions of the external dependencies.
- _End to end tests_ are used to validate the general plumbing of the application.

## Infrastructure as Code

## Continuous Integration
