# Installing OpenShift GitOps Operator

## Prepare the environment

Connect with your administrator user to OpenShift and find what namespaces are available:

![Installing Operator](/img/installingA1.png "Installing Operator")

In the option `Overview -> Projects` Identify if the petclinic project exist:

![Installing Operator](/img/installingAB2.png "Installing Operator")

If it exists, delete it

![Installing Operator](/img/installingAB3.png "Installing Operator")

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

## Accesing to OpenShift GitOps on OpenShift 4.8 or bellow

In version previous to OCP 4.9 ArgoCD is not integrated with OpenShift Authentication, then in these clusters you require get the admin password of ArgoCD, in this case, please, go to OpenShift-gitops project

![Installing Operator](/img/installingE1.png "Installing Operator")

![Installing Operator](/img/installingE2.png "Installing Operator")

After, get the secrets Submenu into Workloads Menu

![Installing Operator](/img/installingE3.png "Installing Operator")

Then, search openshift-gitops-cluster secret

![Installing Operator](/img/installingE4.png "Installing Operator")

Finally on the Data section **copy to clipboard** the admin.password 

![Installing Operator](/img/installingE5.png "Installing Operator")

**Note:** If you is using OCP 4.9+ you can use the OpenShift credentials

# Accessing to OpenShift GitOps Webconsole on Openshift 4.9

In order to access to OpenShift on version 4.9+ access to Application menu and select **Cluster Argo CD**

![Installing Operator](/img/installingC6.png "Installing Operator")

ArgoCD is preconfigured for authentication using OpenShift permissions. 

![Installing Operator](/img/installingC7.png "Installing Operator")

Then, you can start the application using your current user and password.

![Installing Operator](/img/installingC8.png "Installing Operator")

Additionally, you can grant access to the user via the Authorization interface.

![Installing Operator](/img/installingD2.png "Installing Operator")

And finally, you can access to OpenShift GitOps interface.

![Installing Operator](/img/installingD3.png "Installing Operator")

[Go to content](content.md)
[Go to readme](../README.md)