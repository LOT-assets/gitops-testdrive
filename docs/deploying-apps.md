# Deploying a simple application on Cluster

The application to deploy is PetClinic, this application is stored on 
https://github.com/LOT-assets/gitops-testdrive.git on petclinic-app/02-petclinic

The goal in this section is navigate and deploy this applicaction on the cluster.

# Start ArgoCD Console

Login on Your OpenShift Cluster using userX/*password*

![Deploying Application](/img/deployappsA01.png "Deploying Application")

You can navigate the Quick Tour to understand the menus and main options from the developer's perspective.

![Deploying Application](/img/deployappsA02.png "Deploying Application")

Select the project and go to the Topology menu

![Deploying Application](/img/deployappsA03.png "Deploying Application")

Navigate and look at the description of the pods currently deployed on the right menu.

![Deploying Application](/img/deployappsA04.png "Deploying Application")

ArgoCD installs the CDR required to deploy and maintain ArgoCD clusters. In the current environment, already, there is a cluster deployed with the necessary permission to admin the application on your namespace.

On GitOps Server deployment, you can identify on OpenShift Route that exposes the ArgoCD URL; please open the URL on another tab, logging using OpenShift Login, and confirm your credentials and the authorization data.

![Deploying Application](/img/installingC7.png "Deploying Application")

Verify that has access to the ArgoCD console

![Deploying Application](/img/installingD3.png "Deploying Application")

Create a new application

![Deploying Application](/img/deployappsA1.png "Deploying Application")

Write the following data in the General section:

* Application name: petclinic
* Project: default
* Sync Policy: Manual

![Deploying Application](/img/deployappsA2.png "Deploying Application")

Complete the source and destination

*Source*

* Repository URL: https://github.com/LOT-assets/gitops-testdrive.git
* Revision: HEAD
* Path: petclinic-app/02-petclinic

*Destination*

* Cluster URL: https://kubernetes.default.svc
* Namespace: *userX*

Note: replace userX by your current namespace

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

* What objects was created?
* Where is located the application?
* What is the application objective?

[Go to content](content.md)
[Go to readme](../README.md)