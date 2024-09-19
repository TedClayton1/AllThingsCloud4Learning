## How IAP works

When an application or resource is protected by IAP, it can only be accessed through the proxy by [principals](https://cloud.google.com/iam/docs/overview#concepts_related_identity), also known as users, who have the correct [Identity and Access Management (IAM) role](https://cloud.google.com/iam/docs/understanding-roles). When you grant a user access to an application or resource by IAP, they're subject to the fine-grained access controls implemented by the product in use without requiring a VPN. When a user tries to access an IAP-secured resource, IAP performs authentication and authorization checks.

[App Engine](https://cloud.google.com/iap/docs/concepts-overview#app-engine)[Cloud Run](https://cloud.google.com/iap/docs/concepts-overview#cloud-run)[Compute Engine](https://cloud.google.com/iap/docs/concepts-overview#compute-engine)[GKE](https://cloud.google.com/iap/docs/concepts-overview#gke)[On-premises](https://cloud.google.com/iap/docs/concepts-overview#on-premises)

![diagram of request path to App Engine when using Cloud IAP](https://cloud.google.com/iap/images/iap-app.png)

### Authentication

Requests to your Google Cloud resources come through App Engine, Cloud Load Balancing (External and Internal HTTP(S) Load Balancing). The serving infrastructure code for these products checks if IAP is enabled for the app or backend service. If IAP is enabled, information about the protected resource is sent to the IAP authentication server. This includes information like the Google Cloud project number, the request URL, and any IAP credentials in the request headers or cookies.

Next, IAP checks the user's browser credentials. If none exist, the user is redirected to an OAuth 2.0 Google Account sign-in flow that stores a token in a browser cookie for future sign-ins. If you need to create Google Accounts for your existing users, you can use [Google Cloud Directory Sync](https://support.google.com/a/answer/106368) to synchronize with your Active Directory or LDAP server.




dentity-Aware Proxy (IAP) is ==a Google Cloud product that manages access to applications and resources by using a user's identity and the context of a request==. IAP can be used to protect access to applications hosted on Google Cloud, other clouds, and on-premises applications. 

Here are some benefits of using IAP: 

- Central authorization
    
    IAP establishes a central authorization layer for applications accessed by HTTPS. This allows for an application-level access control model instead of relying on network-level firewalls. 
    
- Simplified for cloud admins
    
    IAP can secure access to apps faster than implementing a VPN. 
    

- Simplified for remote workers
    
    End users can access IAP-secured applications by pointing their web browser to an internet-accessible URL. 
    

- Policy scaling
    
    IAP policies can be defined centrally and applied to all applications and resources across an organization. 
    

IAP can be used to create policies that:

- Confirm application integrity and sensitivity

- Confirm time and date accessibility

- Limit or halt access if a user's location is deemed incorrect, inappropriate, or insecure

- Request additional forms of authentication

- Integrate data from user and entity behavior analytics (UEBA)