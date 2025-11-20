# github-actions-demo


**Why GitHub Actions ?** 

*Simplified Tool Management*:
	+ With GitHub Actions, you don't need to worry about installing and configuring third-party tools like Java, Maven, or Node.js on your CI/CD server. You can simply use pre-built actions to run your application. This eliminates the need for manual tool management, reducing maintenance overhead and allowing you to focus on development.
	+ GitHub Actions provides a large marketplace of pre-built actions that you can use in your workflows. These actions are maintained by the community, so you can benefit from the expertise and contributions of others.

*Centralized Artifact Management*:
	+ GitHub Actions allows you to store all your artifacts, including code, dependencies, and build artifacts, in one place. This eliminates the need to manage multiple storage locations and makes it easier to track and manage your pipeline.
	+ With GitHub Actions, you can also store your pipeline configuration files alongside your code. This provides a single source of truth for your pipeline and makes it easier to collaborate with team members.

*Streamlined Development Process*:
	+ GitHub Actions enables fast-paced development and frequent deployments by automating your CI/CD pipeline. You can automate tasks like testing, building, and deployment, allowing you to deliver new features and updates quickly and reliably.
	+ With GitHub Actions, you can also set up complex workflows that involve multiple jobs and steps. This allows you to automate complex processes and ensure that your code is properly tested and validated before deployment.

*Single Source of Truth*:
	+ GitHub Actions provides a single source of truth for your codebase, pipelines, and configurations. By storing your pipeline configuration files alongside your code, you can ensure that everyone on your team has access to the same pipeline configuration.
	+ This also makes it easier to manage changes to your pipeline. You can use GitHub's version control features to track changes and collaborate with team members.

*Advantages of Writing GitHub Action Scripts in YAML*

*Human-readable*: YAML is a human-readable format, making it easy to understand and edit workflow files.
*Platform-agnostic*: YAML is a platform-agnostic format, meaning that you can use the same workflow file on different operating systems and environments.
*Version-controlled*: Since workflow files are stored alongside your code, you can version-control them just like your code. This allows you to track changes and collaborate with team members.
*Flexible*: YAML is a flexible format that allows you to define complex workflows with multiple jobs and steps.
*Easy to learn*: YAML is a widely-used format, and many developers are already familiar with it. This makes it easy to learn and start using GitHub Actions.

*Example GitHub Actions Workflow File*

Here's an example GitHub Actions workflow file (.yml) that demonstrates a simple CI/CD pipeline:
```
name: Build and Deploy

on:
  push:
    branches:
      - main

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Build
        run: |
          mvn clean package

      - name: Deploy
        uses: actions/deploy@v1
        with:
          environment: production
```
This workflow triggers on push events to the main branch, checks out the code, builds the project using Maven, and deploys it to production. The workflow file is written in YAML and defines a single job with multiple steps.


<img width="1920" height="1080" alt="Screenshot (526)" src="https://github.com/user-attachments/assets/19760bbd-dafd-460b-9f48-86057f1285cb" />

<img width="1920" height="1080" alt="Screenshot (527)" src="https://github.com/user-attachments/assets/270554f6-4512-4d2b-b4cb-0e6d5d60c33a" />

<img width="1920" height="1080" alt="Screenshot (528)" src="https://github.com/user-attachments/assets/a2de7d91-35c6-4b60-9903-6cbccb28d3ac" />

<img width="1920" height="1080" alt="Screenshot (529)" src="https://github.com/user-attachments/assets/2dd5d5f1-8aca-44f5-8329-621a1145cafd" />

In the following picture notice the "Checkout Repo" and "Post Checkout Repo".

<br><br>
<img width="1920" height="1080" alt="Screenshot (531)" src="https://github.com/user-attachments/assets/517f98f2-4e80-47bf-8547-fe17ca01ed06" />
