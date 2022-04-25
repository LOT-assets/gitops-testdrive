# Mantaining "Single Source of Truth"

## Discovering differences

Navigate to OpenShift Developer perspective and navigate the application

![Single Source of Truth](/img/operationsA1.png "Single Source of Truth")

Change the configuration of deployment *petclinic*, search the section replicas, and change to 2 replicas.

![Single Source of Truth](/img/operationsA2.png "Single Source of Truth")

Go to ArgoCD webconsole and identify the points out of synchronization

![Single Source of Truth](/img/operationsA3.png "Single Source of Truth")

Select Sync and restore the application.

![Single Source of Truth](/img/operationsA4.png "Single Source of Truth")

## Maintain the synchronization of the application

Go to ArgoCD Webconsole and edit the configuration

![Single Source of Truth](/img/operationsB1.png "Single Source of Truth")

Change the Synchronization from *Manual* to *Automatic*

![Single Source of Truth](/img/operationsB2.png "Single Source of Truth")

Go to OpenShift Developer perspective and modify the configuration of deployment.

![Single Source of Truth](/img/operationsB3.png "Single Source of Truth")

What happened with the application?

## Deploying changes from GitHub

In this section go to adjust the application to you own Github repository and promote changes from the repository

Navigate to https://github.com/LOT-assets/gitops-testdrive.git

![Single Source of Truth](/img/operationsF1.png "Single Source of Truth")

Login on GitHub and fork the repository

![Single Source of Truth](/img/operationsF2.png "Single Source of Truth")

![Single Source of Truth](/img/operationsF3.png "Single Source of Truth")

Get the URL from new Repository

![Single Source of Truth](/img/operationsF4.png "Single Source of Truth")

![Single Source of Truth](/img/operationsF5.png "Single Source of Truth")

On ArgoCD WebConsole modify the application and put the URL from the new Repository

At this moment, the application is synchronized with your repository on HEAD revision. Promote changes to the main branch via commit or pull request and evaluate how the changes are applied to the application.

[Go to content](content.md)
[Go to readme](../README.md)