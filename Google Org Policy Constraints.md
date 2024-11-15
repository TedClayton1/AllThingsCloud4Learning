
A constraint is **a particular type of restriction against a Google Cloud service or a list of Google Cloud services**. Think of the constraint as a blueprint that defines what behaviors are controlled. For example, you can restrict project resources from accessing Compute Engine storage resources using the compute.

I.E An Org wants you to restrict the team to only the us-central-1 region


Google Cloud's organization policy constraints are ==restrictions that can be applied to Google Cloud resources==: 

- **What they are**
    
    Organization policy constraints are restrictions, or rules, that can be applied to Google Cloud resources. These constraints can be set at the organization, folder, or project level, and apply to the resource and any child resources. 
    
- **How they work**
    
    Organization policies work hierarchically, meaning that rules set at a parent resource apply to child resources. 
    
- **Types of constraints**
    
    There are two types of constraints: list and boolean. List constraints evaluate against a list of allowed or denied values, while boolean constraints are either enforced or not enforced. 
    
- **Examples of constraints**
    
    Some examples of organization policy constraints include:
    
    - **Restricting TLS versions**: This constraint only applies to requests using TLS, and can be used to specify which TLS versions are allowed or denied. 
        
    - **Restricting which projects can supply KMS CryptoKeys**: This constraint can be used to specify which projects can be used to supply Customer-Managed Encryption Keys (CMEK). 
        
    
- **Custom constraints**
    
    Users can create custom organization policies to enforce more granular restrictions. Custom constraints can include a name, resource name, RESTful methods, condition, action, display name, and description. 
    

Organization policies can be combined with policies set at resource or identity scopes, which can lead to competing permissions and constraints.

