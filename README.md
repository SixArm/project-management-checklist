# Project Checklist

* Enable remote tools. For example, Google Drive, Dropbox, ScreenHero, Git, etc.

* Create style guide. (Versioned and in central location)

## Project Management

Setup:

* Document any communication about the project with other stakeholders.

* Document any kinds of existing code, frameworks, libraries, processes, approvals, etc.

* Document any integration points. For example, does the project involve any other projects, products, applications, endpoints, imports/exports, feeds, email lists, group chat forums, etc.?

* Document any stakeholders. For example, who are the people involved in the project? Are there other people who may be related to the project's goals, such as coworkers building other projects, or organization partners, or third-party vendors, etc.? If the organization is large and diverse, then be sure to check widely.

* Create a stakeholder value map.

* Create a plan for AAAA: authentication, authorization, auditing, accounting. For example, how does a user sign in, what credentials are expected, what entitlements are expected, etc. For example, consider Attribute-Based Access Control (ABAC) or its slightly less-powerful equiavent Role Based Access Control (RBAC).

Ongoing:

* Create a place for useful links. For example, create a shared document, or a blog post, or an intranet page.

Business:

* Create a domain model.


## Coding

* Create a coding style guide. For example, one way is to create demonstration source code with embedded annotations, to show developers how to create classes, frameworks, modules, feature toggles, metrics, analytics, etc.

* Create a "Hello World" app. The goal of the app is to prove it's runnable. Stand it up. Do the same with any of the related requirements, such as a "Hello World" database, a "Hello World" API gateway, etc.

* Regularly groom the code to ensure it is idiomatic. If it's not, then fix it. This is especially important on projects where team members are new to the coding language and/or the coding tooling.

* Create a plan for handling "tech debt". Distinguish between true tech debt (e.g. we're using a free trial license that will expire in 30 days) versus false tech debt (e.g. we're writing sub-par code and sometime in the future we'll clean it up). Document the debt in the source code repository so it lives with the code.

* Decide on team work practices. For example, pair programming (e.g. when do people pair, how often, why), remote working, expectations for rush work, etc.

* Decide on a general approach for code overlaps. For example, Rails uses the ActiveRecord pattern to essentially provide complete code overlap between a model and its storage. For example, a more-complex project may have separate classes for view models, business logic models, and data storage models.


## Git

Setup:

* Create any hooks, such as a pre-commit hook, or post-commit hook.

* Set up git alias commands. See http://gitalias.com

* Decide if/how to use git submodules for project components. Generally, there's a major benefit to using submodules, in return for a learning curve.

* Document how the project uses feature toggles.

Flow:

* Decide on a git branch strategy. For example, decide on how a developer can start a topic, submit a topic, finish a topic, etc.

* Document preferred git tactics. For example, does the team want tiny commits (e.g. fix a typo), or small commits (e.g. fix all typos), or medium commits (e.g. create a new feature), or large commits (e.g. create a new framework).


## Testing

Setup:

* Gather best practices and current thinking. For example, ask peers, read blogs, and research state of the art.

* Consider any testing frameworks, such as RSpec for Ruby, or Appium for mobile apps, etc.

* Write guidelines of testing plans. For example, create examples of unit testing, test doubles such as mocks and stubs, code coverage goals, etc.

Test Driven Development:

* Write example of seed data. For example, how to fill an empty database table with data rows that must exist for the app to run.

* Write example of how to create a test object. For example, create a factory or fixture.

* Describe the kinds of testing that are wanted. For example, what is a unit test, a functional test, an integration test, a UI test, etc.

* Explain how to share test data between tests. For example, how can a developer re-use a test object among a unit test, functional test, integration test, etc.

* Create UI testing strategy. For example, how to do it, how much is desired, how to monitor results, etc.

* Ensure testing is sufficiently discrete. For example, use randomized data for identifiers, strings, and test ordering. For example, ensure that testing of controllers can run separately from models, and testing of models can run separately from  databases.

Integration:

* Document a strategy for continuous integration (CI) and continuous delivery (CD).

* Decide quality goals. For example, what are the expectations of the continuous integration build always succeeding? What happens if it fails?

* Decide on what happens if a test fails. For example, if the test causes a segmentation fault, can the testing framework produce a core dump suitable for inspection?


## Data

Setup:

* Decide on data storage basics. For example, what data is planned, what is reasonably expected, where does the data live, and so forth.

* Decide on terminology. For example, different organizations use the word "schema" to mean different things.

* Document any work on connecting data sources to data sinks. For example, if the project is storing data in a traditional back office SQL database, and also providing a mobile client app, how does the data get from the database to the app, and vice versa?

* Decide on how to handle different data needs for the development, testing, and production deployments. For example, consider creating two kinds of testing databases: one that is suitable for a developer to use for local tests, and which contains a small amount of fake data, and one that is suitable for a continuous integration server to use for regression tests, and which contains a santized snapshot of the entire production data set.

Import/Export:

* Decide on any goals for data import or data export. For example, does the project load data from a CSV file, or TSV file, or external web source such as a REST API?


## Mobile

Setup:

* Decide generally if the goal is to produce a native-looking application. For example, does the project want an Apple iOS app to use Apple iOS standard components or custom components? For example, does the project want an Android app to use Google Material Design or custom design?

Scope limits:

* First get the project working on the most important device, using the most important configuration. For example, on an Apple iOS project, first get the project working on the iPhone (not the iPad), on the current model (not an older model), using portrait orientation (not landscape orientation), etc.

Xcode:

* Decide on file management: use Xcode groups, or filesystem directories, or both?

* Decide what to do when constraint warnings happen: ignore them, or fix them.
