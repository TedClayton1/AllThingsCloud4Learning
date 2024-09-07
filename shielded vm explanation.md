

Shielded VMs are ==virtual machines (VMs) that have additional security controls to protect them from threats like [[rootkits and bootkits]]==. They are available on cloud platforms like Google Cloud Platform and Microsoft Azure.  

Here are some of the security features of Shielded VMs:  

- Secure boot: Verifies the digital signature of each boot component against a secure store of approved keys. Any boot component that isn't signed properly or at all won't be allowed to run.  
    
- Virtual Trusted Platform Module (vTPM): Securesly measures a Hyper-V host's boot process and code integrity policy.  
    
- Integrity monitoring: A feature provided by vTPM.  
    
- Logging: Malicious actions by insiders within an organization are logged.  
    

Shielded VMs use a combination of hardware and software-based security features to protect VMs from the moment they start up until they are running. If you applied a system update on a VM instance, you should update the [[integrity policy baseline]]. 