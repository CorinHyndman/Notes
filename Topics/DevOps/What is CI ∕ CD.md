___
**CI/CD** stands for **Continuous Integration** and **Continuous Delivery/Deployment**.  
It is a modern software development practice that automates the process of **building, testing, and deploying** code changes. By integrating frequently and automating delivery, teams achieve faster and more reliable software releases.
___
###### Keywords
- **CI (Continuous Integration)**
    - Practice of merging all developers’ working copies to a shared mainline several times a day.
    - Each integration triggers automated builds and tests.
- **CD (Continuous Delivery)**
    - Automates the release process to ensure code can be deployed to production at any time.
- **CD (Continuous Deployment)**
    - Extends Continuous Delivery by automatically deploying every successful build to production.
- **Pipeline**
    - A sequence of automated steps (build → test → deploy).
- **Build**
    - The process of compiling source code and preparing artifacts.
- **Test**
    - Running automated tests to ensure code quality.
- **Deploy**
    - Releasing the build to staging or production environments.
- **Artifact**
    - A compiled or packaged piece of software ready for deployment (e.g., `.jar`, `.zip`, [[Docker|.docker]] image).
- **Workflow**  
    - A defined set of steps triggered by specific events (like a push to `main`).
- **Trigger**
    - An event that starts a pipeline run (e.g., code push, pull request, or scheduled job).
___
## Typical Pipeline Stages
1. **Source / Version Control**
	- Code changes are committed and pushed to a repository (e.g., [[Git Explained|Github]]).
2. **Build Stage**
    - Source code is compiled and dependencies are installed.
    - Example: `npm install`, `mvn package`, or `docker build`.
3. **Test Stage**
    - Automated unit, integration, and UI tests run.
    - Ensures the build is stable and functional.
4. **Artifact / Packaging**
    - Build output is stored as an artifact (e.g., `.jar`, `.zip`, or container image).
5. **Deploy / Release Stage**
    - The verified artifact is deployed to staging or production.
    - Can be manual (delivery) or automatic (deployment).
6. **Monitor / Feedback**
    - System logs and metrics are monitored to detect issues post-deployment.
___
![[ci-cd-pipeline-explained.jpg]]
![[ci-cd-pipeline.png]]
![[continuous-deployment-delivery.webp]]
___
## Flashcards
#flashcards

**What does CI/CD stand for?** :: Continuous Integration and Continuous Delivery/Deployment.

**What is the goal of Continuous Integration?** :: To frequently integrate code into a shared repository and automatically test each integration.

**What is Continuous Delivery?** :: Automating the release process so the software can be deployed at any time with one command.

**What is Continuous Deployment?** :: Automatically deploying every code change that passes all stages of the pipeline to production.

**What are the main stages of a CI/CD pipeline?** :: Source → Build → Test → Deploy → Monitor.

**What is an artifact in CI/CD?** :: A packaged build output (like a `.jar`, `.zip`, or Docker image) ready for deployment.

**What’s the difference between Continuous Delivery and Continuous Deployment?** :: Delivery requires manual approval to deploy; Deployment pushes automatically after tests pass.

**What are common CI/CD tools?** :: Jenkins, GitHub Actions, GitLab CI/CD, CircleCI, Travis CI, Azure Pipelines, Bitbucket Pipelines.

**What is a pipeline trigger?** :: An event that starts the pipeline (e.g., code push, pull request, or scheduled run).

**Why is CI/CD important?** :: It reduces integration issues, improves code quality, and speeds up release cycles.

**What does a failed build usually indicate?** :: A problem in compilation, tests, or configuration that must be fixed before proceeding.

**What happens during the test stage of a CI/CD pipeline?** :: Automated tests are executed to validate that new code doesn’t break existing functionality.

**How can you roll back a failed deployment?** :: Use versioned artifacts or previous container images to restore a stable release.
___