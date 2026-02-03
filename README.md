# Java Web App Deployment with AWS CI/CD

Welcome to this project combining Java web app development and AWS CI/CD tools!

<br>

## Table of Contents
- [Introduction](#introduction)
- [Technologies](#technologies)
- [Contact](#contact)
- [Conclusion](#conclusion)

<br>

# Introduction
This project is used for an introduction to creating and deploying a Java-based web app using AWS, especially for CI/CD tools.

The deployment pipeline I'm building around the Java web app in this repository is invisible to the end-user, but makes a big impact by automating the software release processes.

## Why This Project?
I'm undertaking this project as part of my journey to become a proficient DevOps engineer. By building this CI/CD pipeline, I'm gaining hands-on experience with industry-standard tools and practices that are essential in modern software development. This project aligns with my career goals of:

- **Mastering Cloud Infrastructure**: Understanding how to leverage AWS services for scalable and reliable application deployment
- **Automating Software Delivery**: Learning to build automated pipelines that reduce manual intervention and human error
- **Bridging Development and Operations**: Gaining practical experience in DevOps practices that are in high demand across the tech industry
- **Building Production-Ready Skills**: Developing expertise that directly translates to real-world enterprise environments

This hands-on experience will strengthen my portfolio and prepare me for future roles where automation, efficiency, reliability and  cloud-native are paramount.

<br>

# Technologies
Here's what I'm using for this project:

- [**Amazon EC2**](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/tree/eef83dbd2e5369c9be370d1db96563a763276e76/01%20-%20Set%20Up%20a%20Web%20App%20in%20the%20Cloud): I successfully developed a web application and performed live deployment on different Amazon EC2 virtual servers, so that software development and deployment were carried out entirely in the cloud.
- [**VS Code**](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/tree/eef83dbd2e5369c9be370d1db96563a763276e76/01%20-%20Set%20Up%20a%20Web%20App%20in%20the%20Cloud): For my IDE, I chose Visual Studio Code. It connects directly to my development EC2 instance, making it easy to edit code and manage files in the cloud.
- [**GitHub**](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/tree/eef83dbd2e5369c9be370d1db96563a763276e76/02%20-%20Connect%20a%20Github%20Repo%20with%20AWS): All my web app code is stored and versioned in this GitHub repository.
- [**AWS CodeArtifact**](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/tree/eef83dbd2e5369c9be370d1db96563a763276e76/03%20-%20Store%20Dependecies%20in%20CodeArtifact): I have successfully configured AWS CodeArtifact as a secure repository for my web application packages, as well as how to managed and store these packages in one central location. This ensures that verified package versions are used during the application build and deployment process.
- [**AWS CodeBuild**](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/tree/eef83dbd2e5369c9be370d1db96563a763276e76/04%20-%20Contionus%20Integration%20with%20Codebuild): I successfully implemented the Continuous Integration (CI) method with CodeBuild, automating the process of converting code into deployable packages and ensuring that applications are built consistently and correctly as an important part of the CI/CD pipeline.
- [**AWS CodeDeploy**](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/tree/eef83dbd2e5369c9be370d1db96563a763276e76/05%20-%20Deploy%20a%20Web%20App%20with%20CodeDeploy): I used AWS CodeDeploy to automate the process of deploying these files to the web server so that the application could be accessed by users and most importantly, I learned to implement disaster recovery techniques by performing deployment rollbacks.
- [**CloudFormation Infrastructure As Code (IAC)**](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/tree/eef83dbd2e5369c9be370d1db96563a763276e76/06%20-%20Infrastructure%20as%20Code%20with%20CloudFormation) : I implemented AWS CloudFormation to perform provisioning and infrastructure as code (IaC) management on Production environment resources and Development Environment resources.
- [**AWS CodePipeline**](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/tree/eef83dbd2e5369c9be370d1db96563a763276e76/07%20-%20Build%20a%20CICD%20Pipeline%20with%20AWS): CodePipeline will orchestrate a *Continuous Integration(CI)* and *Continuous Deployment(CD)* workflow system to automate the entire process from GitHub to CodeDeploy, integrating build, test, and deployment steps into one efficient workflow.

## Challenges & Solutions

Throughout this project, I've encountered several challenges and found effective solutions:

### [Challenge 1: Resolving 403 Permission Denied Error](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/blob/main/02%20-%20Connect%20a%20Github%20Repo%20with%20AWS/Connect%20a%20GitHub%20Repo%20with%20AWS.md#challange-resolving-403-permission-denied-error) 
**Problem**: This error indicates an authentication issue where Git was using cached credentials from a different GitHub account instead of the correct account. 

**Solution**: cleared the cached credentials and updated the remote URL

### [Challenge 2: Got Failure at running Deployments](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/blob/main/05%20-%20Deploy%20a%20Web%20App%20with%20CodeDeploy/Deploy%20a%20Web%20App%20With%20CodeDeploy.md#-challange--got-failure-at-running-deployments)

**Problem**: During my initial deployment attempt, I encountered a critical failure when initiated deployment

**Solution**: Set up an intallation Agent on Instance and Configured the neccessary policies and role for permission to related resources.

### [Challenge 3: get mismatch error when created resource with CloudFormation](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/blob/main/06%20-%20Infrastructure%20as%20Code%20with%20CloudFormation/IAC%20with%20CloudFormation.md#template-testing)

**Problem**: get missmatch error when initial stack deployment.

**Solution**: modified configuration harcoded template.

### [Challenge 4: encountered an error that prevented CodePipeline from performing rollbacks](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange/blob/main/07%20-%20Build%20a%20CICD%20Pipeline%20with%20AWS/Build%20a%20CICD%20Pipeline%20with%20AWS.md#-challenge-fixing-rollback-permissions)

**Problem**: The CodePipeline service role lacked explicit permission to retrieve application revisions from CodeDeploy.

**Solution**: added an inline policy to the CodePipeline service role granting the necessary permissions

# Contact
If you have any questions or comments about the NextWork Web Project, please contact:

**Ngurah Gede Wisnu Gudakesa**  
📧 Email: [ngurahgedewisnugk@gmail.com](mailto:ngurahgedewisnugk@gmail.com)  
💼 LinkedIn: [Connect with me on LinkedIn](https://www.linkedin.com/in/ngurahgedewisnugk)  
<img width="24" height="24" alt="GitHub_Invertocat_Black_Clearspace" src="https://github.com/user-attachments/assets/fb10e584-0260-4346-b915-7575c01c80c5" />
 Github: [Visit my github](https://github.com/ngurahgdewisnugk)


# Conclusion
Thank you for exploring this project! I'll continue to build this pipeline and apply my learnings to future projects.

This project represents a significant milestone in my DevOps journey, demonstrating my ability to work with cloud infrastructure, automation tools, and modern software delivery practices. The skills gained here—from infrastructure setup to pipeline automation—are directly applicable level-up to DevOps and Cloud-Native Orchestration roles.

A big shoutout to **[NextWork](https://learn.nextwork.org/app)** for their project guide and support. [You can get started with this DevOps series project too by clicking here.](https://learn.nextwork.org/projects/aws-devops-vscode?track=high)

---

### Related Projects
For a comprehensive view of my DevOps learning journey, check out my **[7-Day DevOps Challenge](https://github.com/ngurahgdewisnugk/7-Days-Devops-Challange)** repository, which documents my daily progress through various DevOps concepts and AWS services.
