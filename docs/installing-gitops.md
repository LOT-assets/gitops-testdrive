# Installing OpenShift GitOps Operator

## Prepare the environment

Connect with your administrator user to OpenShift and find what namespaces are available:

![Installing Operator](/img/installingA1.png "Installing Operator")

In the option Overview -> Projects

Identify if the nginx-basic project does not exist:

![Installing Operator](/img/installingA2.png "Installing Operator")

If it exists, delete it

![Installing Operator](/img/installingA3.png "Installing Operator")

## Install the OpenShft Pipelines Operator

Go to the Operators section and select Operatorhub

![Installing Operator](/img/installingB2.png "Installing Operator")

Search for GitOps and identify OpenShift GitOps

![Installing Operator](/img/installingB3.png "Installing Operator")

Select the Red Hat OpenShift GitOps operator and select the install option

![Installing Operator](/img/installingC1.png "Installing Operator")

Keep the default options and select Install again

![Installing Operator](/img/installingC2.png "Installing Operator")

The operator will start to install, please wait a couple of minutes until it finishes

![Installing Operator](/img/installingC3.png "Installing Operator")

When the operator is installed you will see a message like the following:

![Installing Operator](/img/installingC4.png "Installing Operator")

Once installed validate that an ArgoCD instance was deployed in the openshift-gitops project

![Installing Operator](/img/installingC5.png "Installing Operator")

# Accessing to OpenShift GitOps Webconsole

In Application menu select **Cluster Argo CD**

![Installing Operator](/img/installingC6.png "Installing Operator")

ArgoCD is preconfigured for authentiction using OpenShift permissions. 

![Installing Operator](/img/installingC7.png "Installing Operator")

Then, you can start the application usign your current user and password.

![Installing Operator](/img/installingC8.png "Installing Operator")

Additionally you can grant access to the user via Authorization interface.

![Installing Operator](/img/installingD2.png "Installing Operator")

And finally, you can access to OpenShift GitOps interface.

![Installing Operator](/img/installingD3.png "Installing Operator")

## Accesing to GitOps via argocd cli

The next steps guide in the installation and use of argocd user cli.



[Go to content](content.md)
[Go to readme](../README.md)