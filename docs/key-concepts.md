# Key concepts

## Pre-requisities
To understand the GitOps concept, you require to understand the basic concepts of Linux, containers, and Kubernetes. A good site to get this knowledge is https://kubebyexample.com/

## What is GitOps?
GitOps is a set of practices to manage infrastructure and application configurations using Git, an open source version control system. GitOps works by using Git as a single source of truth for declarative infrastructure and applications.

GitOps uses Git pull requests to automatically manage infrastructure provisioning and deployment. The Git repository contains the entire state of the system so that the trail of changes to the system state are visible and auditable.

GitOps is built around the developer experience and helps teams manage infrastructure using the same tools and processes they use for software development. Other than Git, GitOps gives you the ability to choose the tools you need.

Weaveworks is credited with creating the term GitOps.

## How to get started with GitOps
To get started with GitOps you need infrastructure that can be declaratively managed. Because of this, GitOps is often used as an operating model for Kubernetes and cloud native application development and can enable continuous deployment for Kubernetes.

But using Kubernetes is not a requirement of GitOps. GitOps is a technique that can be applied to other infrastructure and deployment pipelines.   

GitOps can be used to build development pipelines, code applications, manage configurations, provision Kubernetes clusters, and deploy on Kubernetes or container registries.

## What is a GitOps workflow?
GitOps can be considered an evolution in Infrastructure as Code (IaC) that uses Git as the version control system for infrastructure configurations. IaC often follows a declarative approach to infrastructure management by defining the desired state of the system and tracking the system’s actual state.

As with IaC, GitOps requires you to *declaratively describe the desired state of the system.* By using declarative tools, all of your configuration files and source code can be version controlled in Git.

CI/CD pipelines are usually triggered by an external event, like code being pushed to a repository. In a GitOps workflow, changes are made using *pull requests* which modify state in the Git repository. 

To roll out a new release using a GitOps workflow, a pull request is made in Git, which makes a change to the declared state of the cluster. The GitOps operator, which sits between the GitOps pipeline and the orchestration system, picks up the commit and pulls in the new state declaration from Git.   

Once the changes are approved and merged, they will be applied automatically to the live infrastructure. Developers can continue to use their standard workflow and continuous integration/continuous delivery practices. 

When using GitOps with Kubernetes, the operator will often be a Kubernetes Operator.

The operator compares the desired state in the repository to the actual state of the deployed infrastructure. The operator will update the infrastructure whenever a difference is noticed between the actual state and what exists in the repository. The operator can also monitor a container image repository and make updates in the same way to deploy new images.

Observability, which refers to any system that can be observed, is an important concept in GitOps. Observability in GitOps lets you ensure that the desired state and the observed state (or actual state) are the same. 

Using pull requests and a version control system like Git introduces visibility into the deployment process. It lets you view and track any changes made to a system, provides an audit trail, and gives you the ability to rollback changes if something breaks.

GitOps workflows can increase productivity and the velocity of development and deployments, while improving the stability and reliability of systems.

## How is GitOps different from DevOps?
GitOps and DevOps do share some of the same principles and goals. DevOps is about cultural change and providing a way for development teams and operations teams to work together collaboratively.

GitOps gives you tools and a framework to take DevOps practices, like collaboration, CI/CD, and version control, and apply them to infrastructure automation and application deployment. 

Developers can work in the code repositories they already know, while operations can put the other necessary pieces into place.

[Go to content](content.md)
[Go to readme](../README.md)