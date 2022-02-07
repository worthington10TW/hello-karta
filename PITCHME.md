# Get to production!

[https://github.com/worthington10TW/hello-karta](https://github.com/worthington10TW/hello-karta)
Matthew Worthington

<!---
Note:

- Developer @ ThoughtWorks
- Twitter: worthington10
-->

---

## Prerequisites

- VueCli
- HerokuCli
- CircleCI
- Git
- ~~Docker~~
- Powershell/ bash & cUrl
- Node/ Npm

<!---
Note:

- GitHub
- Heroku
- CircleCI
-->

---

## What is a CI/CD pipeline?

- Initiates code builds
- Runs automated tests
- Deploys your code

<!---
Note:

- A tool to
  - Automate the software delivery process
- Deploying One change, One artefact
- Promoted through a single pipeline, deployed to many environments

- Details
- A CI/CD pipeline helps you automate steps in your software delivery process
- One artefact, promoted through a single pipeline, deployed to many environments
-->

---

## Why do we use them?

- Reduce cost of deployment
- Remove manual errors
- Provide standardized feedback loops
- Enable fast product iterations.

<!---
Note:

- Through automation
- increasing delivery confidence and reducing risk
-->

---

## Risk reduction

- Low-risk releases are incremental
- Decouple deployment and release
- Focus on reducing batch size
- Optimize for resilience

<!---
Note:

- Architect decouple systems.
  - Independently releasable changes
  - tight coupling == big-bang risky releases.
- Technical decision to deploy != the business decision
  - Dark releases and feature toggles = Continously deploy 
- 10s of lines of code == easier root cause analysis + service restoration
- Failures are inevitable, move towards rapid service restoration

- Details
- Architect our systems so that we can release individual changes independently, tight coupling will lead to big-bang risky releases.
- Separate the technical decision to deploy from the business decision to launch a feature, so we can deploy continuously but release new features on demand. Two commonly-used patterns that enable this goal are dark launching and feature toggles.
- When each deployment consists of tens of lines of code or a few configuration settings, it becomes much easier to perform root cause analysis and restore service in the case of an incident.
- Failures are inevitable, how do we restore service as rapidly as possible when something goes wrong 
-->

---

## Best practice

- Only build packages once
- Deploy the same way to every environment
- Smoke test your deployments
- Keep your environments similar

<!---
Note:

- Same thing we’ve tested throughout the deployment pipeline
  - eliminating the packages as the source of the failure
- We test the deployment process many times before it gets to production
- Running and available as part of the deployment process.
- Same version of the operating system and middleware packages

- Details
- We want to be sure the thing we’re deploying is the same thing we’ve tested throughout the deployment pipeline, eliminating the packages as the source of the failure.
- We test the deployment process many, many times before it gets to production,eliminating it as the source of any problems.
- Make sure your application is running and available as part of the deployment process.
- Keep your environments similar. Same version of the operating system and middleware packages, configured in the same way. This has become much easier to achieve with modern virtualization, container technology and infrastructure as code.
-->

---

## Triggers

- Code commit
- Scheduled/ CRON
- Manual

<!---
Note:

- Each change in code triggers an automated build-and-test sequence for the given project, providing feedback to the engineering team
- You may want to run tests constantly over a period or perform cleanup tasks
- In some situations a manual triggered pipeline or stage may be necessary, you may require sign-off from QA or have set release dates
-->

---

## ‘You build it, you run it’ 

<!-- @snapend

@fa[rocket fa-5x fa-spin] -->

---

## 1. Build

![Build](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/1.png)

---

## 2. Code quality gate

![Quality gate](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/2.png)

---

## 3. Test automation

![Test](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/3.png)

---

## 4. Publish

![Publish](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/4.png)

---

## 5. Deploy to staging

![Staging](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/5.png)

---

## 6. Smoke tests

![Smoke](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/6.png)

---

## 7. Manual approval

![Manual gate](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/7.png)

---

## 8. Deploy to prod

![Production](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/8.png)

---

## TADA!

![Pipeline](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/pipeline.png)

---

## What will we be using?

![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/babel.png)
![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/cypress.jpeg)
![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/docker.png)
![logo]https://raw.githubusercontent.com/worthington10TW/hello-karta/master/(pitch/tools/github.png)
![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/heroku.png)
![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/mocha.png)
![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/npm.png)
![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/vuejs.png)

---

## What accounts will I need?

![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/circleci.png)
![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/github.png)
![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/heroku.png)

---

## Lets get going

[https://github.com/worthington10TW/hello-karta](https://github.com/worthington10TW/hello-karta)

---

## Validate tools

    ```
    vue --version
    heroku --version
    git --version
    docker --version
    node --version
    npm --version
    curl --version
    ```

---

## Fork

![Fork](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/plan/Fork.png)

[https://github.com/worthington10TW/hello-karta](https://github.com/worthington10TW/hello-karta)

---

## Clone

![Clone](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/plan/Clone.png)

---

## Follow

![Clone](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/plan/Follow.png)

[https://circleci.com](https://circleci.com)

---

## Generate a token

![CreateToken](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/plan/CreateToken.png)

[https://circleci.com/account/api](https://circleci.com/account/api)

---

## You've created your first pipeline!

![FirstPipeline](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/plan/FirstPipelineCombined.png)

---

## Create your apps

### And setup env variables

#### App name < 25 char

```
chmod +x ./.scripts/app-builder.sh
./.scripts/app-builder.sh [Your app name] [circleCI token]
//Or powershell users
./.scripts/app-builder.ps1 [Your app name] [circleCI token]
```

*Did it work?? https://dashboard.heroku.com/apps*
*https://[your-app-name]-staging.herokuapp.com/*
*https://[your-app-name].herokuapp.com/*

---

## Did it work?

[https://[your-app-name].herokuapp.com/](https://[your-app-name].herokuapp.com/)
[https://[your-app-name]-staging.herokuapp.com/](https://[your-app-name]-staging.herokuapp.com/)
![NewApp](pitch/plan/NewApp.png)

---

## Create a vue project

```
cd ..
vue create --preset ./hello-karta/.vue hello-karta
//Merge when prompted
```

*remember to copy package.json from ./.scripts to the root*

---

## VueJS

- Simplicity
- Testable
- Flexibility
- Fast and small

<!---
Note:

- Straightforward template syntax- Handlebars
- Easy to test- mocha/ jest/ jamine
- Component based model- Rich official libraries or make your own
- 30kb, virtual dom- concept same as react

Note:

- Main -> App -> Views -> Components
-->

---

## Cheatsheet

    npm run serve
    npm run test:unit
    npm run test:e2e
    npm run build

---

## Cypress

![logo](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/tools/cypress.jpeg)

Test that the homepage links to the about page

---

## Lets create a pipeline!

![Pipeline](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/pipeline.png)

---

## Circle CI

- Workflows for job orchestration
- First-class Docker support
- Language-agnostic support

<!---
Note:

- Complete control of execution- build, test, deploy
- Docker at its heart
- Supports any language that builds on Linux or macOS

Note:

- True pipelines
- Fan in and out
- Manually triggers
- Visible feedback
- Branch filtering
-->

---

## Get to staging

![Manual gate](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/7.png)

---

## Get to prod

![Pipeline](https://raw.githubusercontent.com/worthington10TW/hello-karta/master/pitch/pipeline/pipeline.png)

---

## New requirement

- As a user
- I want to see how many times I click a button
- So that I can test out my amazing TDD skills

---

## New requirement

- As a user
- I want to see how many times I click a button
- So that I can test out my amazing TDD skills

*The ticker starts at 0*
*The ticker state is not persisted*
*Ticker to increment by on each click*
