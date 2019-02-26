# Development Best Practices

## Collaboration

When contributing please first discuss the change you wish to make via issue, slack, email, or any other method with the owners of this repository before making a change.

Please note we have a code of conduct, please follow it in all your interactions with the project.

## Github

### Gitflow Workflow

In each of our projects, we try to adhere to the guidelines of the **Gitflow Workflow**. Essentially this means that the vast majority of our work and collaboration with take place on/in the `develop` branch for a project. Pull requests should be created for any/all work that will get merged into the develop branch through “feature” branches that are named/referenced by their JIRA ticket number (ex: `feature/user-login-PROJ-123`).

### README

READMEs are vital to the ongoing health and collaboration of a project especially as new teams and members are onboarded. A README, at the minimum, should include a Getting Started, Running the Tests, and Deployment sections. Those sections should cover step-by-step how a new developer can get a local development environment installed, configured and up and running. 

It is imperative that these steps be fairly detailed with any specific versioning information, commands or startup scripts that should be used. Even if some of these steps can/could be inferred due to common conventions it is best to error on side of caution and assume a developer might be new to or unfamiliar with this exact environment / tech stack. 

### Linting

To detect and avoid linting and formatting errors we often use **eslint**, **stylelint**, **prettier**, and/or similar plugins/extensions for a given code editor. 

### Contributing

When contributing, please ensure that the commit message follows the [conventional commit spec](https://www.conventionalcommits.org/en/v1.0.0-beta.2/):

`$ git commit -m "type: subject reference"`

Where `subject` is the commit message (lowercase with no ending period), `reference` is the JIRA id PROJ-XX, and `type` is any of the types (listed below) describing the intent of the commit.

### Pull Requests

Ensure any install or build dependencies are removed before the end of the layer when doing a build.

Update the README.md with details of changes to the interface, this includes new environment variables, exposed ports, useful file locations and container parameters, etc.

Pull Requests can be merged in once you have the sign-off of two other developers, or if you do not have permission to do that, you may request the second reviewer to merge it for you.

### Wiki

The project Wiki should be used as a catch-all for any and all information related to the project. Architecture, Designs, Domains, Server Configuration, Important logic / workflows, 3rd party integrations, etc should all be added to the Wiki to be referenced as needed. 

Usernames / Passwords for any and all systems or integrations should be added to a private Google Doc/Sheet and referenced / linked within the Wiki. 

Typical Wiki sections are listed below and should be used if applicable.

### Highlights / References

* [Gitflow Workflow](https://datasift.github.io/gitflow/IntroducingGitFlow.html)
* README Sections (at a minimum)
  * Getting Started
    * Prerequisites
    * Environment Variables
    * Local Environment Setup
  * Running the Tests
    * End to end tests
    * Code style / Lint tests
  * Deployment
    * How to deploy to Staging/Production/etc environments
* Linting
  * [eslint](https://eslint.org/)
  * [stylelint](https://stylelint.io/)
  * [prettier](https://prettier.io/)
* Contributing commit message `types`:
  * build
  * chore
  * ci
  * docs
  * feature
  * fix
  * perf
  * refactor
  * revert
  * style
  * test
* Wiki
  * Home
  * Getting Started (usually links to README)
  * Architecture
    * API Documentation
      * Apiary link(s)/reference(s)
    * System Architecture Diagram
    * Schema Diagram
  * Design Screens
    * InVision links
    * Zeplin links
    * Direct links (gdrive, dropbox, etc)
  * Documents / Sheets (links)
  * Domain Information
    * Registrar
    * DNS
    * IP address(es)
    * Subdomains
  * Environments
  * Server Info/Configuration
  * How to Use
    * Libs, scripts, rake tasks, etc
  * 3rd Party Integrations (examples)
    * Fastlane
    * CircleCi
    * Sendgrid
  * Testing
    * Summary / Notes
    * Code Coverage
    * CI/CD pipeline
  * Analytics
  * History
    * Versions
    * Change Log

## Testing

We do **not** aim for 100% test coverage. We largely follow and encourage “test driven” or “test first development” but this is not a strict rule. Our goal with testing is to cover main code paths and important business logic. Additionally if a bug is found or an error/exception encountered, that is usually a good indication of something that should be covered by a test going forward. 

Pull requests should have 100% passing tests before they are merged. If there is a good reason this can not achieved raise the issue with the team and we will decide if this one-off case can be ignored.

## Continuous Integration

At a minimum, Continuous Integration should be configured to automatically run tests on every Pull Request into the `develop` and `master` branches.

Pull Requests from develop => to => master should usually include tagging and versioning bumps.

## Code of Conduct

### Our Pledge

In the interest of fostering an open and welcoming environment, we as contributors and maintainers pledge to making participation in our project and our community a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, gender identity and expression, level of experience, nationality, personal appearance, race, religion, or sexual identity and orientation.

### Our Standards

Examples of behavior that contributes to creating a positive environment include:

* Using welcoming and inclusive language
* Being respectful of differing viewpoints and experiences
* Gracefully accepting constructive criticism
* Focusing on what is best for the community
* Showing empathy towards other community members

Examples of unacceptable behavior by participants include:

* The use of sexualized language or imagery and unwelcome sexual attention or advances
* Trolling, insulting/derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others' private information, such as a physical or electronic address, without explicit permission
* Other conduct which could reasonably be considered inappropriate in a professional setting
