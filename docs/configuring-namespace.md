# Prepare the project to GitOps

## Prepare the OpenShift project to deploy the application

The application to deploy on Openshift will be stored on a project called petclinc. In this case, the administrator must be build the project and add the respective permission to ArgoCD user.

### Create the project petclinc

In the Home Menu, select projects option

![Deploying Application](/img/configuringA1.png "Deploying Application")

Then, select Create Project in the top-right side

![Deploying Application](/img/configuringA2.png "Deploying Application")

Use petclinic in the name and display name. *Note:* The name must be on lower case and only use (-) simbol

![Deploying Application](/img/configuringA3.png "Deploying Application")

### Grant access to petclinic project 

Go to RoleBindings section on *User Management* Menu

![Deploying Application](/img/configuringB1.png "Deploying Application")

The create a new RoleBonding, in order to grant *edit* access to openshift-gitops-argocd-application-controller Service Account to Petclinic namespace.

![Deploying Application](/img/configuringB2.png "Deploying Application")

Create the Role Binding with the next data:
* Binding Type: Namespace Role Binding
* Name: petclinic-gitops
* Namespace: petclinic
* Role: edit
* Subject: Service Account
* Subject Namespace: openshift-gitops
* Subject Name: openshift-gitops-argocd-application-controller

![Deploying Application](/img/configuringB3.png "Deploying Application")

The RoleBinding is created and GitOps get access to modify the components on the project

[Go to content](content.md)
[Go to readme](../README.md)