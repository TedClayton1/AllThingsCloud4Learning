➤  Deployment Manager is an infrastructure deployment service that automates the creation and management of Google Cloud resources. Deployment is a single unit of multiple resources, which will work as a whole 

➤  User can use Deployment Manager to create a set of Google Cloud resources and manage them as a unit, called a deployment. 

➤  Deployment Manager use Conﬁguration ﬁle(YAML) to deﬁne the resource and Deployment Properties.  

➤  User can use Jinja & Python templates to parameterize the conﬁguration and allow reuse of common deployment params such as a load balanced, auto-scaled instance group. 

➤  Conﬁguration ﬁle can be re-used to create the Same Set of Resource over and over again. Google Cloud Platform : Cloud Training

➤  Deployment Manager Conﬁg File Sample - 
resources: 
- name: example-vm 
  type: compute.v1.instance 
  properties: 
     zone: europe-west1-b 
     machineType: zones/europe-west1-b/machineTypes/n1-standard-1 
    disks: 
    … 
➤  Each listed resource always has a type, which is the kind of resource that will be created (a VM, an IP address, etc.), a name, and properties describing with what parameters the resource should be created. Google Cloud Platform : Cloud Training

➤  Deployment Manager Conﬁg File Sample - 
resources: 
- name: example-vm 
  type: compute.v1.instance 
  properties: 
     zone: europe-west1-b 
     machineType: zones/europe-west1-b/machineTypes/n1-standard-1     disks: 
    … 
➤  Conﬁguration ﬁle describes all the resources you want for a single deployment. 

➤  A conﬁguration must contain a resources: section.Google Cloud Platform : Cloud Training

➤  Component of Resource Section:  

➤  name- A user-deﬁned string to identify this resource

➤  type - The type of the resource being deployed such as compute.v1.instance, compute.v1.disk. 

Supported Resource Types 
➤  properties - The parameters for this resource type. They must match the properties for the type such as zone: asia- east1-a, boot: true.Google Cloud Platform : Cloud Training

➤  Create Deployment- 
gcloud deployment-manager deployments create <DEPLOYMENT_NAME> --conﬁg <YAML_FLE>

➤  Update Deployment- User can preview any changes in Deployment before commit it. 

gcloud deployment-manager deployments update 
<DEPLOYMENT_NAME> --conﬁg <YAML_FLE> --preview 

update - 
gcloud deployment-manager deployments update 
<DEPLOYMENT_NAME>

Cancel preview - 
gcloud deployment-manager deployments cancel-preview 
<DEPLOYMENT_NAME>Google Cloud Platform : Cloud Training

➤  Add Label to Deployment- 
gcloud deployment-manager deployments create 

<DEPLOYMENT_NAME> --conﬁg <YAML_FLE> --labels devserver=backend,storage=media 

➤  Describe Deployments. 
gcloud deployment-manager deployments describe 
<DEPLOYMENT_NAME>

➤  Delete Deployment - 
gcloud deployment-manager deployments delete 
<DEPLOYMENT_NAME>