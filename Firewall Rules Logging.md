
Firewall rules logging is ==a tool that records how a firewall manages traffic, and can be used to analyze, audit, and verify the effectiveness of firewall rules==. Firewall logs can be used for a variety of purposes, including: 

- **Network security**
    
    Firewall logs can help identify suspicious network activity, such as unauthorized connections from specific sources. They can also help ensure compliance by logging all allowed and blocked connections. 
    
- **Troubleshooting**
    
    Firewall logs can help identify problems during troubleshooting. For example, if a service is experiencing connectivity issues, firewall logs can help determine if the firewall is the cause. 
    
- **Security incidents**
    
    After a security incident, firewall logs can help identify the method used to attack and possibly provide information about the attacker. 
    
- **Malicious sources**
    
    Firewall logs can help identify and block malicious sources that try to intrude on a network. 
    

Firewall logs record details about each connection, including: Source and destination IP addresses, Protocol and ports, Date and time, and Identity of the firewall rule that applied to the traffic. 

To make firewall logs easier to analyze, it's recommended to implement logging standards that ensure all logs are consistent. This includes determining which events to log, how to aggregate, store, and analyze data, and the maximum storage size. 

- [](https://cloud.google.com/firewall/docs/firewall-rules-logging#:~:text=Firewall%20Rules%20Logging%20lets%20you,that%20applied%20to%20the%20traffic.)
    
    Firewall Rules Logging | Cloud NGFW
    
    Firewall Rules Logging lets you audit, verify, and analyze the effects of your firewall rules. For example, you can determine if a...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAACjUlEQVR4AWKgBIyCV86mHCBMZ0tNALTVQ4AdQRSF4WCwiW3btm3btr2JzW1s27btLLPJ2OxodPPXGFXDzuJ7fnXObXYidAXO4EqsM1ihvvtfk5aJDf0OSQO/abRE/ceu8Da4hwhIOkXgHtpkZVM7sUA//IFklGvn1nJs9NqwDuutfh3WWU6ZmbwHXCCZcXjsRum9ykMo4IIemdnnPhADCx/YSvcU9RpW3OSEq+DEfFAmveEO3h0bb0sl/BFGeHdoVAkFYlVSn+FRosmTWmdt49khPQWa+XRu5OI3pLYETK4qQXMqSvDi8hI4o7IEzqz07PfBfOXC7znmMF0X+q1020WQBUnGBc3SLBAwrvqy0PUl5M/J3BJ2w1kIixZ2N5ofrx9gnun/TFoE51SoxjJjcNg9BycW7hF22ylIBaaBMg63eK6jLcH+NmwFH/TQnhUqHC6QDHiDfIYS9zQF9GcFi5SBDySD3rDlihgKrEocbDwrWMSBRbZlJhz11BqGApMShxrPChapwf78pgmwcAFNUA1j+N0r0+SaAvnQAhdgaQp867A+tIYq0IPFLE2BCwQWSHag1uKze4bJDWdFaIHYEpKMhR6qwBCIRgu77qaxW0I0hhgLqGltK7DOqmUswCYdZNgC45DDhulzYJzhQByktkAH+GkKvEIdGwrUwStIUqF+6KAOrCIE3Ute4C+X3nc3i1qNTg3ch1VaJ4ZvUOe7WegOnkMgGvfUZTvuWjAveYFPNwvL8LOdhKBUsVBmJb2fqGt73OQqvNPpXsZQGwrc0t0L6uDNZ/PkdhV4A/2xRYF8vc90P9Hw1EA/+wuog846gnypHrWE50EHFj8FLxsKeOGUOuLxb3zo9o2CUQAAQTP7qwJoUEkAAAAASUVORK5CYII=)
    
    Google Cloud
    
- [](https://www.exabeam.com/explainers/event-logging/firewall-logs/#:~:text=A%20firewall%20monitors%20traffic%20into,to%20help%20investigate%20an%20attack.)
    
    The Significance and Role of Firewall Logs - Exabeam
    
    A firewall monitors traffic into and out of the environment it was developed to protect. Some firewalls also offer visibility into...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAB9klEQVR4AWIYHmAUAIirA4iGwigMw7lmJpMkTJIkYUImhDAEkkASkoREgSQkhCSBkBAlTBKGkCRJQhKShCQkJJlkMhl/71L5HJLb1oYHvDrfrbprtawCJRvP2cZIqR5gDA5pRIs93oxXuE9bxRwP4QKuJD8BxpbgxHAxx7vNeBLaOxH5r/EaPMr4Haqk1+IJe/AKPe5hT8aziJt+IH2i0A8wCSfmTJ8yfaaQ463IyPETBKS34U36sfZ8x8O4luPPaDQfxTfSU6j/7qMumO8DrMGJAWk5CdP7ZDxnEz1/He81xxPQ3m/6un45w0NwSKHO73g9UnL8FhXSG/As/RphGW/CC9ynhJ/xAI7k+BvaTD+RnkGr/t5xJuMZtPh5gBk4MW36rOmT5ke/ACfG/Yy3m1fqEJ70OLLS97Uz1oGsjO9AexyVP41X4laOP6FOehXupD+iRo5X417GHxCRHsEDNmDHP2zCiR7Tk6Z3m1duG050SvewK23APsCgOb5i+rDpy+b3PmbGF00fN31OjzfhRY5fISw9irT0S5TL8Wa8yvFzhKTHkJF+iuDX8SBOzSsVs/8JERD6RxXChRxPI2q+ew8B4enxeTjx6ytjji/BiRE/r1yHeaV24fkY7zLjSfj6uI3hfW5IWIhE35sBsQcSFmAYSmAUAABjXu6SuMcp9QAAAABJRU5ErkJggg==)
    
    Exabeam
    
- [](https://documentation.meraki.com/MX/Firewall_and_Traffic_Shaping/Firewall_Logging#:~:text=The%20Firewall%20Log%20is%20a,the%20rules%20are%20functioning%20correctly.)
    
    Firewall Logging - Cisco Meraki Documentation
    
    Aug 22, 2024 — The Firewall Log is a monitoring tool that displays the outcomes of traffic after it has been evaluated by Layer 3 and...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAMAAABEpIrGAAAAZlBMVEV4smZrqlhurFxgpEtkp1BhpUxcokZbokVipU1YoEKu0aPw9++z1KlXoEGQwIH///+ZxItUnj5QmziGunaNvn6rz6DP48nK4MKfyJH2+vXq8+iAt2+nzZvb69fl8eJ6s2jY6NLD3bvOsKwVAAAA+UlEQVR4AczSRYKFMAwAUCBtaPAK7ve/5JDy3dYTrPKoB0H4M6IghJ8hDiB/xP8CGMMPoICiiEB9BYBJmmYAX0FelEdUOeQ5cjOkUT0BnTDIDFgLqIACF9IzqBkk1JRlC0hdXw4jvYOp4ndnov74zIjvwHe00FpyOK1eQX3WVHrmz0bwCjLT8Gc2lYdWvwN3aXzhT0vwBvBs3HT86Ud6BVpfGseBP3v+BlCejRuf7wN6WUkttW98wTDlb6GvgKzP5xLF4tv2f6RRfAUQd/MyIdOxGXaBoLJls3Q/MEBS5XweFKEgVApJAD2fKLyeAPwbssCQyRcceAELAAmQH9SN8f6OAAAAAElFTkSuQmCC)
    
    Cisco Meraki Documentation
    
- Show all
    

Generative AI is experimental.

## Featured snippet from the web