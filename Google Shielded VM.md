
A Google Shielded VM is ==a virtual machine (VM) that uses secure boot capabilities to protect against malware and rootkits==. Shielded VMs use a vTPM to provide a virtual root-of-trust, which verifies the VM's identity and ensures it's part of the specified project and region. 

||Google Shielded VM|
|---|---|
|Protection|Protects against boot- and kernel-level malware and rootkits|
|Verification|Uses a vTPM to verify the VM's identity and ensure it's part of the specified project and region|

Virtual machines use virtualization technology to create a virtual version of a computer on a physical machine. The physical machine is called the host, and the VMs running on it are called guests. 

In the Google Cloud console, the gcloud command-line tool, and the REST API, the terms Compute Engine instance, virtual machine instance, VM instance, and VM are used interchangeably.