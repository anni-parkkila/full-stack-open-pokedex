# Exercise 1

Let's consider an application written in Ruby, by a team of ~6 people.

## Linting, testing, building

Two popular options for linting Ruby code are [RuboCop](https://rubocop.org/) and [Prettier for Ruby](https://github.com/prettier/plugin-ruby). Prettier is especially popular in JavaScript ecosystem, and it uses a predefined set of rules for linting and does not allow custom rules or exceptions. However, it takes care of formatting automatically. RuboCop on the other hand focuses on code formatting for Ruby projects. It has extensive configuration options and allows customization. It also performs static analysis and enforces a set of code quality rule, which helps catching potential issues and improving the overall code quality.

Three main types of tests to test Ruby code are unit tests, integration tests and acceptance tests. Unit tests are used to test only small, isolated parts of the code, like individual methods or classes. Integration tests are used to test how the different components of the system work together, e.g. by testing how different classes or modules interact with each other. Acceptance tests are used to test the system as a whole from the user's perspective. This could mean testing the system through its user interface or API. It's a good idea to use all of these test types for the application.

Ruby code has no need for the build step.

## Alternatives to CI besides Jenkins and GitHub Actions

Another popular CI/CD provider is [CircleCI](https://circleci.com/). It is a cloud-based platform, and can be integrated with into GitHub repositories. For each repository a new project needs to be set up to the system, and a configuration file added to the root of each repository. In that file it is possible to configure which steps and tests need to be run e.g. on individual branches and when merging to master.

## Self-hosting vs cloud-based

One thing to consider, of course, is the price for both options. Self-hosting is not completely free either, and there are some aspects to consider when thinking of the costs. For example, if the hardware the server is running on breaks, it can cause downtime to the application and that way affect whatever income coming from the app. Self-hosting also requires some manual work with software updates. Self-hosting mainly has benefits in larger companies with multiple teams and projects. Considering that this example application only has 6 developers, the application is most likely not so huge that self-hosting would be necessary. It'd probably be better use of the developers' time to do the setup as cloud-based, and not having to worry as much about backups, updates, patches etc.
