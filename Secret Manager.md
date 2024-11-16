
# Secret Manager overview 



Secret Manager is a secrets and credential management service that lets you store and manage sensitive data such as API keys, usernames, passwords, certificates, and more.

A [_secret_](https://cloud.google.com/secret-manager/docs/creating-and-accessing-secrets) is a global resource that contains a collection of metadata and secret versions. The metadata can include labels, annotations, and permissions.

A [_secret version_](https://cloud.google.com/secret-manager/docs/add-secret-version) stores the actual secret data, such as API keys, passwords, or certificates. Each version is identified by a unique ID or timestamp.

Using Secret Manager, you can do the following:

- **Manage rollback, recovery, and auditing using versions**: Versions help you manage gradual rollouts and emergency rollback, If a secret is accidentally changed or compromised, you can revert to a previous, known-good version. This minimizes potential downtime and security breaches. Versioning maintains a historical record of changes made to a secret, including who made the changes and when. It helps you audit secret data and track any unauthorized access attempts. You can pin secret versions to specific workloads and add [aliases](https://cloud.google.com/secret-manager/docs/assign-alias-to-secret-version) for easier access to secret data. You can also [disable](https://cloud.google.com/secret-manager/docs/disable-secret-version) or [destroy](https://cloud.google.com/secret-manager/docs/destroy-secret-version) secret versions that you don't require.
    
- **Encrypt your secret data in transit and at rest**: All secrets are encrypted by default, both in transit using TLS and at rest with AES-256-bit encryption keys. For those requiring more granular control, you can encrypt your secret data with [Customer-Managed Encryption Keys (CMEK)](https://cloud.google.com/secret-manager/docs/cmek). Using CMEK, you can generate new encryption keys or import existing ones to meet your specific requirements.
    
- **Manage access to secrets using fine-grained Identity and Access Management (IAM) roles and conditions**: With [IAM roles and permissions](https://cloud.google.com/secret-manager/docs/access-control), you can [provide granular access](https://cloud.google.com/secret-manager/docs/manage-access-to-secrets) to specific Secret Manager resources. You can segregate responsibilities for accessing, managing, auditing, and rotating secrets.
    
- **Ensure high availability and disaster recovery with secret replication**: You can [replicate your secrets](https://cloud.google.com/secret-manager/docs/choosing-replication) across multiple regions to ensure high availability and disaster recovery for your applications regardless of their geographic location. You can choose between the following replication policies:
    
    - [Automatic replication](https://cloud.google.com/secret-manager/docs/choosing-replication#automatic): Google decides the regions considering availability and latency. You are only charged for one location.
        
    - [User managed replication](https://cloud.google.com/secret-manager/docs/choosing-replication#user-managed): You can select a custom set of regions depending on your requirements. You are charged per location.
        
- **Rotate secrets automatically to meet your security and compliance requirements**: [Rotating your secrets](https://cloud.google.com/secret-manager/docs/rotation-recommendations) protects against unauthorized access and data breaches. Regularly changing your secrets reduces the risk of stale or forgotten secrets and ensures compliance with many regulatory frameworks that require periodic rotation of sensitive credentials.
    
- **Enforce data residency using regional secrets**: [Data residency](https://cloud.google.com/architecture/framework/security/data-residency-sovereignty) requires that certain types of data, often belonging to specific individuals or organizations, be stored within a defined geographic location. You can create [regional secrets](https://cloud.google.com/secret-manager/docs/create-regional-secrets) and store your sensitive data within a specific location to comply with data sovereignty laws and regulations.