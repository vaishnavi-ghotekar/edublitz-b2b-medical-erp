So my last project was from the pharmaceutical domain. It was basically an ERP application developed for a pharmaceutical manufacturing company. The main purpose of the application was to manage inventory, orders, resources, and overall internal operations of the company.

The total project duration was 13 months, and we were a team of 7 people. In that, I was the only DevOps Engineer, so I handled the complete DevOps lifecycle from scratch like starting from repository creation till final deployment and production maintenance.

Talking about the tech stack, the frontend was developed using React.js, and the backend consisted of 3 microservices developed using Java and Spring Boot. For the database, we used MongoDB Atlas, which is a managed NoSQL database service.

From the deployment perspective, we followed a cloud-native architecture on AWS. The frontend application was hosted on Amazon S3 and exposed through CloudFront CDN for faster content delivery. We integrated the client domain using Route 53 and managed SSL certificates through ACM.

For the backend, we containerized all the microservices using Docker and pushed the images to Amazon ECR. Then we deployed those services on Amazon EKS, which is Kubernetes managed by AWS. We used Kubernetes Ingress and Load Balancer to expose the backend APIs externally. So basically, whenever the frontend communicates with the backend, it uses dedicated subdomains routed through the ingress.

If I talk about the branching strategy, we followed a proper Git workflow with multiple branches like develop, testing, UAT, production, feature, and hotfix branches.

The developers were not allowed to directly push into the develop branch. They always created feature branches, implemented changes, and raised Pull Requests. We had mandatory code reviews before merging any PR.

After sprint completion, the develop branch was merged into the testing branch where QA team performed testing. If any bugs were found, they raised Jira tickets, and developers fixed them in the next sprint cycle.

Once QA approved the application, the code was promoted to the UAT branch where stakeholders and clients performed User Acceptance Testing. Finally, after approval from all stakeholders, the UAT branch was merged into the production branch for the live release.

We also maintained hotfix branches. Whenever any critical issue came in production, we created a hotfix branch directly from production, fixed the issue, and merged it back safely.

For project management, we followed Agile methodology and used Jira for sprint planning, task management, bug tracking, and documentation tracking.

From the DevOps side, we used GitHub for source code management, Terraform for Infrastructure as Code, Docker for containerization, Jenkins for CI/CD, ECR for image storage, and EKS for orchestration.

On AWS, we used services like:

* EKS
* ECR
* S3
* CloudFront
* Route 53
* ACM
* IAM
* Load Balancer
* Auto Scaling

For CI/CD automation, I configured Jenkins pipelines from scratch. The pipeline mainly had 4 stages:

* Pull
* Build
* Test
* Deploy

In the pull stage, the source code was fetched from GitHub.

In the build stage, Docker images were created and pushed to Amazon ECR.

In the testing stage, we integrated SonarQube for code quality analysis and Trivy for vulnerability scanning.

Finally, in the deployment stage, the application was deployed on Amazon EKS.

We also integrated GitHub webhooks with Jenkins, so whenever developers pushed code to a specific branch, the corresponding pipeline triggered automatically without any manual intervention.

For the development environment, deployments were automatic. But for testing, UAT, and production environments, we implemented manual approval stages to ensure controlled releases.

Talking about my responsibilities, I was involved in complete infrastructure planning, tool selection, repository planning, and branching strategy discussions.

I managed GitHub repositories, access control, SSH keys, tokens, PR reviews, and merge conflict resolution.

I also wrote and maintained Terraform scripts for the complete infrastructure provisioning and ensured that all infrastructure changes happened only through Terraform.

Apart from that, I wrote Dockerfiles for all microservices, Kubernetes manifest files, ingress configurations, and deployment files.

I was also responsible for setting up and maintaining the Jenkins server and CI/CD pipelines. If any pipeline failed, troubleshooting and fixing it was part of my daily responsibilities.

Additionally, documentation management was also handled by me. I maintained technical documentation, tracked issue resolutions, monitored ticket updates, and documented root cause analysis for critical incidents.

Overall, this project gave me strong hands-on experience in AWS, Kubernetes, Terraform, Jenkins, Docker, CI/CD automation, Git workflows, and production-level DevOps practices.
