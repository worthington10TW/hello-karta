# Get to production!

Matthew Worthington

Note:

- Developer @ ThoughtWorks
- Twitter: worthington10

---

## What is a CI/CD pipeline?

- initiates code builds
- runs automated tests
- deploys your code

Note:

- A CI/CD pipeline helps you automate steps in your software delivery process
- One artefact, promoted through a single pipeline, deployed to many environments

---

## Why do we use them?

- remove manual errors
- provide standardized development feedback loops
- enable fast product iterations.

## Triggers

- code commit
- scheduled/ CRON
- manual

Note:

- Each change in code triggers an automated build-and-test sequence for the given project, providing feedback to the engineering team
- You may want to run tests constantly over a period or perform cleanup tasks
- In some situations a manual triggered pipeline or stage may be necessary, you may require sign-off from QA or have set release dates
