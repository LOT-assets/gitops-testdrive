# Mantaining "Single Source of Truth"

## Discovering differences

Navigate to OpenShift Developer perspective and navigate the application


Change the configuration of deployment *petclinic*, search the section replicas, and change to 2 replicas.


Go to ArgoCD webconsole and identify the points out of synchronization

Select Sync and restore the application.

## Maintain the synchronization of the application

Go to ArgoCD Webconsole and edit the configuration


Change the Synchronization from *Manual* to *Automatic*


Go to OpenShift Developer perspective and modify the configuration of deployment


What happened with the application?

## Deploying changes from GitHub

In this section go to adjust the application to the own Github repository and promote changes from the repository

Navigate to https://github.com/jcepedav/gitops-testdrive

Login on GitHub and fork the repository

On ArgoCD WebConsole modify the application and put the URL from the new Repository

In this moment the application is synchronized with your own repository on HEAD revision. Promove changes to main branch via commit or pull request and evaluate how the changes are applied to application.


[Go to content](content.md)
[Go to readme](../README.md)