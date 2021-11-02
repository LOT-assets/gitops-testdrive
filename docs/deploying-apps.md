# Deploying a simple application on Cluster

The application to deploy is PetClinic, this application is stored on 
https://github.com/jcepedav/gitops-testdrive on petclinic-app/02-petclinic

The goal in this section is navigate and deploy this applicaction on the cluster.

# Start ArgoCD Console

Go to ArgoCD web console using Applications Menu from OpenShift

![Deploying Application](/img/installingC6.png "Deploying Application")

Logging using user admin and admin password or OpenShift Login

![Deploying Application](/img/installingC7.png "Deploying Application")

Verify that has access to ArgoCD console

![Deploying Application](/img/installingD3.png "Deploying Application")

Create a new application

![Deploying Application](/img/deployappsA1.png "Deploying Application")

Write the follow data in General section:

* Application name: petclinic
* Project: default
* Sync Policy: Manual

![Deploying Application](/img/deployappsA2.png "Deploying Application")

Complete the source and destination

*Source*

* Repository URL: https://github.com/jcepedav/gitops-testdrive
* Revision: HEAD
* Path: petclinic-app/02-petclinic

*Destination*

* Cluster URL: https://kubernetes.default.svc
* Namespace: petclinic

![Deploying Application](/img/deployappsA3.png "Deploying Application")

Finally, maintain the values of Kustomize as the image

![Deploying Application](/img/deployappsA4.png "Deploying Application")

Select **Create** in the top of screen and wait to application Syncronize

![Deploying Application](/img/deployappsA4.png "Deploying Application")

The application is present on the main ArgoCD Main Screen

![Deploying Application](/img/deployappsA5.png "Deploying Application")

Select Sync over the petclinc application and confirm default options

![Deploying Application](/img/deployappsA7.png "Deploying Application")

When tha application is syncronized, go to OpenShift and explore the application

![Deploying Application](/img/deployappsA8.png "Deploying Application")

On OpenShift go to Developer perspective and identify all objects created

What objects was created?
Where is located the application?
What is the application objective?

[Go to content](content.md)
[Go to readme](../README.md)