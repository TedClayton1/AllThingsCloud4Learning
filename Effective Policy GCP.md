
In Google Cloud (GCP), an effective policy is ==the combination of a resource's policy and the policies of its parent resources in the resource hierarchy==. This is also known as policy inheritance. For example, if a folder policy overrides a parent policy, the effective policy for resources in the folder will be the folder policy, even if the parent policy is enabled.

*The effective policy is the union of the policy set at the node and policies inherited from its ancestors!