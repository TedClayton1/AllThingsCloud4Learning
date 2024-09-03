A Google service account is a special type of Google account that ==allows applications to access Google APIs and Google Cloud services without human authorization==. Service accounts are managed by Identity and Access Management (IAM) and are often used to run applications, services, or automated processes within an organization's network


* For non human-like for Apps, services

 * Service Account is identity for Compute engine

* Service account keys for authentication

 * Max 10 keys per Service Account 

  * Max 100 Service Account per project


Types of Service Account

1. Google Managed Service Account -automatically created by Google to do things like: patching of a database, VM updates or a migration task like a VM migration from one drone to another drone. 

2. Built-in SA-Compute Engine & App Engine default service accounts - A default service account is created with it. This default service account can always be associated with compute engine instance, or a app engine. Once those service accounts are associated with Compute Engine, anything you can do, and your own personal email ID, or your cloud identity domain email ID is not accountable for what this compute engine will do. Everything will be a responsiblity of this service account. This service account for non-human user but only humans will tend to it.


3.  User created custom SA - Completely under our control. One can use the user created custom SA along with the Built-in SA- Compute Engine & App Engine



