
The integrity policy baseline for a [[Shielded VM]] is ==a known good boot sequence that's used to compare subsequent boots of the VM to determine if anything has changed==. The baseline is created when a VM instance is first booted, and it's based on the boot image that's implicitly trusted. 

Here's how the integrity policy baseline works for Shielded VMs:

- **Creation**
    
    When a VM instance is first booted, Measured Boot creates the integrity policy baseline from the first set of measurements. 
    
- **Storage**
    
    The integrity policy baseline is securely stored. 
    
- **Comparison**
    
    Each time the VM instance boots, measurements are taken again and stored in secure memory until the next reboot. Integrity monitoring compares the most recent boot measurements to the integrity policy baseline. 
    
- **Updates**
    
    The baseline can be updated using the current instance configuration. This is recommended after any planned boot-specific changes, like kernel updates or kernel driver installation. 
    
- **Failures**
    
    If integrity validation fails, the failure is captured as a logged event and raised in Cloud Monitoring. You can investigate the reason for the failure and take action, such as stopping the instance or updating the baseline. 
    

- [](https://cloud.google.com/compute/shielded-vm/docs/shielded-vm#:~:text=This%20information%20identifies%20both%20the,for%20the%20late%20boot%20sequence.)
    
    What is Shielded VM? | Google Cloud
    
    This information identifies both the components that were loaded, and their load order. The first time you boot a VM instance, Mea...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAACjUlEQVR4AWKgBIyCV86mHCBMZ0tNALTVQ4AdQRSF4WCwiW3btm3btr2JzW1s27btLLPJ2OxodPPXGFXDzuJ7fnXObXYidAXO4EqsM1ihvvtfk5aJDf0OSQO/abRE/ceu8Da4hwhIOkXgHtpkZVM7sUA//IFklGvn1nJs9NqwDuutfh3WWU6ZmbwHXCCZcXjsRum9ykMo4IIemdnnPhADCx/YSvcU9RpW3OSEq+DEfFAmveEO3h0bb0sl/BFGeHdoVAkFYlVSn+FRosmTWmdt49khPQWa+XRu5OI3pLYETK4qQXMqSvDi8hI4o7IEzqz07PfBfOXC7znmMF0X+q1020WQBUnGBc3SLBAwrvqy0PUl5M/J3BJ2w1kIixZ2N5ofrx9gnun/TFoE51SoxjJjcNg9BycW7hF22ylIBaaBMg63eK6jLcH+NmwFH/TQnhUqHC6QDHiDfIYS9zQF9GcFi5SBDySD3rDlihgKrEocbDwrWMSBRbZlJhz11BqGApMShxrPChapwf78pgmwcAFNUA1j+N0r0+SaAvnQAhdgaQp867A+tIYq0IPFLE2BCwQWSHag1uKze4bJDWdFaIHYEpKMhR6qwBCIRgu77qaxW0I0hhgLqGltK7DOqmUswCYdZNgC45DDhulzYJzhQByktkAH+GkKvEIdGwrUwStIUqF+6KAOrCIE3Ute4C+X3nc3i1qNTg3ch1VaJ4ZvUOe7WegOnkMgGvfUZTvuWjAveYFPNwvL8LOdhKBUsVBmJb2fqGt73OQqvNPpXsZQGwrc0t0L6uDNZ/PkdhV4A/2xRYF8vc90P9Hw1EA/+wuog846gnypHrWE50EHFj8FLxsKeOGUOuLxb3zo9o2CUQAAQTP7qwJoUEkAAAAASUVORK5CYII=)
    
    Google Cloud
    
- [](https://cloud.google.com/compute/shielded-vm/docs/integrity-monitoring#:~:text=The%20initial%20integrity%20policy%20baseline,stop%20the%20instance%20if%20necessary.)
    
    Monitoring integrity on Shielded VMs | Google Cloud
    
    The initial integrity policy baseline is derived from the implicitly trusted boot image when the instance is created. Updating the...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAACjUlEQVR4AWKgBIyCV86mHCBMZ0tNALTVQ4AdQRSF4WCwiW3btm3btr2JzW1s27btLLPJ2OxodPPXGFXDzuJ7fnXObXYidAXO4EqsM1ihvvtfk5aJDf0OSQO/abRE/ceu8Da4hwhIOkXgHtpkZVM7sUA//IFklGvn1nJs9NqwDuutfh3WWU6ZmbwHXCCZcXjsRum9ykMo4IIemdnnPhADCx/YSvcU9RpW3OSEq+DEfFAmveEO3h0bb0sl/BFGeHdoVAkFYlVSn+FRosmTWmdt49khPQWa+XRu5OI3pLYETK4qQXMqSvDi8hI4o7IEzqz07PfBfOXC7znmMF0X+q1020WQBUnGBc3SLBAwrvqy0PUl5M/J3BJ2w1kIixZ2N5ofrx9gnun/TFoE51SoxjJjcNg9BycW7hF22ylIBaaBMg63eK6jLcH+NmwFH/TQnhUqHC6QDHiDfIYS9zQF9GcFi5SBDySD3rDlihgKrEocbDwrWMSBRbZlJhz11BqGApMShxrPChapwf78pgmwcAFNUA1j+N0r0+SaAvnQAhdgaQp867A+tIYq0IPFLE2BCwQWSHag1uKze4bJDWdFaIHYEpKMhR6qwBCIRgu77qaxW0I0hhgLqGltK7DOqmUswCYdZNgC45DDhulzYJzhQByktkAH+GkKvEIdGwrUwStIUqF+6KAOrCIE3Ute4C+X3nc3i1qNTg3ch1VaJ4ZvUOe7WegOnkMgGvfUZTvuWjAveYFPNwvL8LOdhKBUsVBmJb2fqGt73OQqvNPpXsZQGwrc0t0L6uDNZ/PkdhV4A/2xRYF8vc90P9Hw1EA/+wuog846gnypHrWE50EHFj8FLxsKeOGUOuLxb3zo9o2CUQAAQTP7qwJoUEkAAAAASUVORK5CYII=)
    
    Google Cloud
    
- [](https://cloud.google.com/compute/shielded-vm/docs/automating-responses-integrity-failures#:~:text=integrity%20monitoring%20events.-,Overview,instances%20that%20fail%20integrity%20validation.)
    
    Automating responses to integrity validation failures | Shielded VM
    
    Overview. Integrity monitoring collects measurements from Shielded VM instances and surfaces them in Cloud Logging. If integrity m...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAACjUlEQVR4AWKgBIyCV86mHCBMZ0tNALTVQ4AdQRSF4WCwiW3btm3btr2JzW1s27btLLPJ2OxodPPXGFXDzuJ7fnXObXYidAXO4EqsM1ihvvtfk5aJDf0OSQO/abRE/ceu8Da4hwhIOkXgHtpkZVM7sUA//IFklGvn1nJs9NqwDuutfh3WWU6ZmbwHXCCZcXjsRum9ykMo4IIemdnnPhADCx/YSvcU9RpW3OSEq+DEfFAmveEO3h0bb0sl/BFGeHdoVAkFYlVSn+FRosmTWmdt49khPQWa+XRu5OI3pLYETK4qQXMqSvDi8hI4o7IEzqz07PfBfOXC7znmMF0X+q1020WQBUnGBc3SLBAwrvqy0PUl5M/J3BJ2w1kIixZ2N5ofrx9gnun/TFoE51SoxjJjcNg9BycW7hF22ylIBaaBMg63eK6jLcH+NmwFH/TQnhUqHC6QDHiDfIYS9zQF9GcFi5SBDySD3rDlihgKrEocbDwrWMSBRbZlJhz11BqGApMShxrPChapwf78pgmwcAFNUA1j+N0r0+SaAvnQAhdgaQp867A+tIYq0IPFLE2BCwQWSHag1uKze4bJDWdFaIHYEpKMhR6qwBCIRgu77qaxW0I0hhgLqGltK7DOqmUswCYdZNgC45DDhulzYJzhQByktkAH+GkKvEIdGwrUwStIUqF+6KAOrCIE3Ute4C+X3nc3i1qNTg3ch1VaJ4ZvUOe7WegOnkMgGvfUZTvuWjAveYFPNwvL8LOdhKBUsVBmJb2fqGt73OQqvNPpXsZQGwrc0t0L6uDNZ/PkdhV4A/2xRYF8vc90P9Hw1EA/+wuog846gnypHrWE50EHFj8FLxsKeOGUOuLxb3zo9o2CUQAAQTP7qwJoUEkAAAAASUVORK5CYII=)
    
    Google Cloud
    
- Show all
    

Generative AI is experimental.

## Featured snippet from the web

**The first time you boot a VM instance, Measured Boot creates the integrity policy baseline from the first set of these measurements, and securely stores this data**. Each time the VM instance boots after that, these measurements are taken again, and stored in secure memory until the next reboot.