# 20: GitHub Actions CI/CD Setup

## Your Task

Your task is to take starter code and create a CI/CD pipeline using GitHub Actions to run the component tests via Cypress when a Pull Request is made to the develop branch, and the application is deployed when code is merged from develop to the main branch.

## User Story

```md
AS A software engineer looking to integrate a CI/CD pipeline in a codebase
I WANT a full-stack application that runs test cases when a Pull Request is made to the develop branch and automatically deploys to Render when the code is merged to main
SO THAT I can ensure that all code integrations are clean and pass the proper requirements and that the application is constantly updated when major releases are made to the main branch
Acceptance Criteria
```

## Acceptance Criteria

```md
GIVEN a full-stack application
WHEN I upload new features to the application
THEN I should be making Pull Requests to a develop branch first
WHEN I create a Pull Request to a develop branch
THEN I should be executing a GitHub Action that checks the Cypress component tests
WHEN I see that the tests pass on GitHub Action
THEN I should see those test results on GitHub Action and merge the code
WHEN I push the code from the develop branch to the main branch
THEN I should see that another GitHub Action triggers and should automatically deploy to Render
```

## Mock-Up

Your GitHub Actions for tests should look similar to the image below:

IMAGE 1 GOES HERE

Your GitHub Actions for deployments should look similar to the image below:

IMAGE 2 GOES HERE

## Getting Started

You'll first upload the content inside the Develop folder to a GitHub Repository.

You'll then deploy the application via Render and MongoDB. Use the [Deploy with Render and MongoDB Atlas](https://coding-boot-camp.github.io/full-stack/mongodb/deploy-with-render-and-mongodb-atlas) walkthrough for instructions.

Once you see the application has been deployed, you'll navigate to the Settings option and turn off Auto-Deploy.

**Important**: Make sure to study the application before building upon it. Better yet, start by making a copy of it. It's already a working application&mdash;you're converting it from RESTful API practices to a GraphQL API.

![Animation shows user clicking "Save This Book!" button to save books that appear in search results. The button label changes to "Book Already Saved" after it is clicked and the book is saved.](./Assets/18-mern-homework-demo-02.gif)

Copy the Deploy hook URL as you will need it to properly configure GitHub Actions to deploy to Render.

Next, create a develop branch (either on GitHub directly or via command-line) where all feature branches will be merged to.

**Important**: Your feature branches should always be merged to the develop branch. Only the develop branch should be merged to the main branch.

You will want to have two separate YAML files: one configured to execute GitHub Actions for tests when a Pull Request is made to the develop branch and the other configured to execute GitHub Actions to automatically deploy to Render when develop is merged to main branch.

Use the following resources below:

* [Deploy with Render and MongoDB Atlas](https://coding-boot-camp.github.io/full-stack/mongodb/deploy-with-render-and-mongodb-atlas)
* [Render Deploy Hooks](https://render.com/docs/deploy-hooks)
* [Render API Key](https://render.com/docs/api)
* [Github Repo Secrets](https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions)
* [Main And Develop Branches](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)


## Grading Requirements

> **Note:** If a Challenge assignment submission is marked as “0”, it is considered incomplete and will not count toward your graduation requirements. Examples of incomplete submissions include the following:
>
> * A repository that has no code
>
> * A repository that includes a unique name but nothing else
>
> * A repository that includes only a README file but nothing else
>
> * A repository that only includes starter code

This Challenge is graded based on the following criteria:

### Deliverables: 30%

* A valid URL of your GitHub gist.
* Your GitHub gist that contains the tutorial Markdown. Your gist must include the .md file extension so that your Markdown renders correctly.

### Technical Acceptance Criteria: 50%

Satisfies all of the above acceptance criteria plus the following:

* The GitHub repository must have both a main branch, a develop branch, and use feature branches to submit Pull Requests.
* A GitHub Action must trigger when a Pull Request is submitted to a develop branch and the Action must execute the Cypress component tests.
* All Cypress component tests must pass.
* A GitHub Action must trigger when a Pull Request is submitted and merged to the main branch and the Action must automatically deploy the application to Render.
* The application must be deployed to Render.

### Deployment: 32%

* Application deployed at live URL.
* Application loads with no errors.
* Application GitHub URL submitted.
* GitHub repository contains application code.

### Application Quality: 15%

* User experience is intuitive and easy to navigate.
* User interface style is clean and polished.
* Application resembles the mock-up functionality provided in the Challenge instructions.

### Repository Quality: 13%

* Repository has a unique name.
* Repository follows best practices for file structure and naming conventions.
* Repository follows best practices for class/id naming conventions, indentation, quality comments, etc.
* Repository contains multiple descriptive commit messages.
* Repository contains high-quality README file with description, screenshot, and link to the deployed application.
