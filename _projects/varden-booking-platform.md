---
title: Booking Platform
permalink: customers/varden/booking-platform/
customer: varden
publish: true
short_description: |
    The Booking Platform is a system built to facilitate the integration of the many booking providers available in the healthcare space with Vården's platform. This system allows Vården to quickly integrate new providers and onboard their customers on its platform.
tags:
    - aws
    - lambda
    - docker
    - tye
    - dotnet
    - grpc
    - terraform
    - open telemetry
    - circleci
    - github
    - nuget
reviews:
    - author:
        name: Tobias Nilsson
        title: Integration Architect
      text: |
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec volutpat maximus diam, in suscipit felis hendrerit at. Pellentesque rhoncus tincidunt augue, nec pretium elit. Nulla facilisi. Proin eget aliquet diam. Nullam fermentum nunc lectus, eget convallis diam fringilla at.
---

The Booking Platform is a system built to facilitate the integration of the many booking providers available in the healthcare space with Vården's platform.

When Vården contacted us, they had a need for quickly increase the pace they were able to onboard new booking providers. The Booking Platform solves this need by exposing a unified programming interface to query each provider for available time slots and reserve treatments.

Once built and rolled out, the Vården development team is tasked to take ownership of the platform and expand the park of integrated providers.

### Architecture

The architecture behind the Booking Platform is based on the [IDesign Method][1].  
Following the Method's guidelines, the system is decomposed into several services, each addressing a volatility of the system itself. Moreover, the services are spread across different layers, each layer having a specific role in the overall architecture.

The services composing the system use GRPC to communicate with each other. The Vården's platform can only interact with the Booking Platform via a REST API that exposes the operations available to client systems. The REST API service publishes an OpenAPI specification schema. The schema is used to generate a typed client library that is used by Vården to integrate the calls to the Booking Platform API into their system.

All the services are based on ASP.NET Core 6 and run on the .NET 6 runtime.

### Developer experience

Great care is given to the overall developer experience. Specifically, the whole system is designed to be executed locally with the help of [Microsoft Tye][6]. Furthermore, with the help of tools like [Docker Compose][7], the developers working with this system will be able to execute locally the very same bits that are deployed on production.

Another important aspect of the developer experience is the observability of the system. The Booking Platform was designed with observability in mind so that developers could use traces, logs and metrics to troubleshoot and validate the behavior of the system. The integration of tools like [AWS CloudWatch][2], [AWS X-Ray][3] and [Logz.io][4] via the [OpenTelemetry][5] project gives the developers all the information they need to properly operate the system.

The source code is hosted on GitHub so that developers can leverage the well-known and established [GitHub Flow][15] to collaborate while ensuring the quality is kept in check with the help of pull requests and code reviews.

Finally, the type client library mentioned in the paragraph above is another sign of the importance and care given to the developer experience.

### Continuous integration

Like many modern systems, the Booking Platform has a fully defined continuous integration pipeline that reacts to any change to the main Git repository. The pipeline is managed by [CircleCI][13] and is composed by different jobs depending on whether the change has been pushed to the default branch or to a pull request branch.

The CI pipeline is responsible of building, testing, packaging and deploying the artifacts to the proper environment.

Whilst all changes to the main branch are eventually deployed to the Development environment, GitHub releases are used to initiate the steps of the pipelines to deploy the artifacts into the Staging environment and, after manual approval, to the Production environment.

Tools like the AWS CLI, the AWS tools for PowerShell, the .NET SDK and custom CircleCI orbs are used to perform the different tasks of the pipeline.

### Automated testing

Given the complexity of the platform, several automated testing strategies were adopted to ensure the correctness and overall design of the system.

Each service is accompaigned by a throrough set of unit tests developed with [NUnit][8] with the addition of libraries like [Moq][10] and [AutoFixture][9]. These libraries help reduce the amount of code needed thus making each unit test much more expressive and its intent very clear.

While unit tests ensure that every service is behaving as expected, two layers of integration tests are added to verify that the system as a whole behaves as expected.

The first layer uses the [ASP.NET Core `WebApplicationFactory` helper class][11] to build an in-memory representation of the whole system. While not a true representation of the deployed system, it helps quickly test the integration of all services by [overriding the GRPC networking layer][12].

The second and final layer of integration tests contains most of the tests of the previous layer but targets an instance of the whole system instantiated via Docker Compose. This layer is the closest representation of the system deployed in the cloud environments.

### Infrastructure as Code

Following the most recent cloud engineering best practices, the cloud resources used by the Booking Platform are managed via [Terraform][14].

The Terraform files are stored in another GitHub repository with its own pipeline so that any change to the files are automatically deployed across the different environments.

Finally, a set of modules have been created and [shared on GitHub][16] in order to reduce duplication in this platform infrastructure repository and the ones for future projects.

[1]: https://www.idesign.net/Download/IDesign-Method-Management-Overview.pdf
[2]: https://aws.amazon.com/cloudwatch/
[3]: https://aws.amazon.com/xray/
[4]: https://logz.io/
[5]: https://opentelemetry.io/
[6]: https://devblogs.microsoft.com/dotnet/introducing-project-tye/
[7]: https://docs.docker.com/compose/
[8]: https://nunit.org/
[9]: https://autofixture.github.io/
[10]: https://github.com/Moq
[11]: https://docs.microsoft.com/en-us/aspnet/core/test/integration-tests
[12]: https://renatogolia.com/2021/12/19/testing-asp-net-core-grpc-applications-with-webapplicationfactory/
[13]: https://circleci.com/
[14]: https://www.terraform.io/
[15]: https://docs.github.com/en/get-started/quickstart/github-flow
[16]: https://github.com/vardengho/terraform-modules
