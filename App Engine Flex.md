
App Engine Flex is ==a customizable version of Google App Engine that runs applications in Docker containers on Google Compute Engine virtual machines (VMs)==. It offers more flexibility than App Engine Standard, allowing users to: 

- Use any programming language 
    
- Write to disk 
    
- Use any library 
    
- Run multiple processes 
    
- Choose any Compute Engine machine type 
    
- Take advantage of custom libraries 
    
- Use SSH for debugging 
    
- Deploy their own Docker containers 
    
- Customize the runtime and operating system of their virtual machine 
    
- Use different versions of supported runtimes 
    

Here are some other features of App Engine Flex: 

- Weekly restarts
    
    VM instances are restarted weekly, and Google's management services apply any necessary operating system and security updates. 
    
- Disabled SSH access by default
    
    You can enable root access to your app's VM instances if you choose. 
    
- Routing rules
    
    You can define up to 20 routing rules, each containing the url and service elements. The rules must use HTTP URL patterns that include the " . " notation for separating subdomains. 
    
- Health checks
    
    App Engine logs can indicate if an instance is healthy, unhealthy, lameduck, or app lameduck. 
    
- Budget alerts
    
    You can create budget alerts for the cost of App Engine, including instance hours and RAM. 
    

App Engine Flex can be more expensive than App Engine Standard because you always have to have one instance running 24/7. 

- [
    
    Google App Engine flexible environment docs
    
    Customizable infrastructure - App Engine flexible environment instances are Compute Engine virtual machines, which means that you ...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAACjUlEQVR4AWKgBIyCV86mHCBMZ0tNALTVQ4AdQRSF4WCwiW3btm3btr2JzW1s27btLLPJ2OxodPPXGFXDzuJ7fnXObXYidAXO4EqsM1ihvvtfk5aJDf0OSQO/abRE/ceu8Da4hwhIOkXgHtpkZVM7sUA//IFklGvn1nJs9NqwDuutfh3WWU6ZmbwHXCCZcXjsRum9ykMo4IIemdnnPhADCx/YSvcU9RpW3OSEq+DEfFAmveEO3h0bb0sl/BFGeHdoVAkFYlVSn+FRosmTWmdt49khPQWa+XRu5OI3pLYETK4qQXMqSvDi8hI4o7IEzqz07PfBfOXC7znmMF0X+q1020WQBUnGBc3SLBAwrvqy0PUl5M/J3BJ2w1kIixZ2N5ofrx9gnun/TFoE51SoxjJjcNg9BycW7hF22ylIBaaBMg63eK6jLcH+NmwFH/TQnhUqHC6QDHiDfIYS9zQF9GcFi5SBDySD3rDlihgKrEocbDwrWMSBRbZlJhz11BqGApMShxrPChapwf78pgmwcAFNUA1j+N0r0+SaAvnQAhdgaQp867A+tIYq0IPFLE2BCwQWSHag1uKze4bJDWdFaIHYEpKMhR6qwBCIRgu77qaxW0I0hhgLqGltK7DOqmUswCYdZNgC45DDhulzYJzhQByktkAH+GkKvEIdGwrUwStIUqF+6KAOrCIE3Ute4C+X3nc3i1qNTg3ch1VaJ4ZvUOe7WegOnkMgGvfUZTvuWjAveYFPNwvL8LOdhKBUsVBmJb2fqGt73OQqvNPpXsZQGwrc0t0L6uDNZ/PkdhV4A/2xRYF8vc90P9Hw1EA/+wuog846gnypHrWE50EHFj8FLxsKeOGUOuLxb3zo9o2CUQAAQTP7qwJoUEkAAAAASUVORK5CYII=)
    
    Google Cloud
    
    
    
    ](https://cloud.google.com/appengine/docs/flexible#:~:text=Customizable%20infrastructure%20%2D%20App%20Engine%20flexible,of%20CPU%20and%20memory%20configurations.)
    
- [
    
    Streaming with Remix on Google Cloud Platform (App Engine ...
    
    Jun 9, 2024 — App Engine Flexible is a more custom version of App Engine. Their documentation does mention a setting that could make ...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAC20lEQVR4AcSQAQaEQBSGB1UCCMDuBbrEQoDoFikAHSR0kJBQ1ygkYfcAuwCB179Pdhi1W9au+vhgzMz7PKFwYlP2yhKLP0vs7TXjLGZc2DuLnXxMM1+c5fCdvctNpCwOMmXF7cCAKyvowABiBQ52eWiaJoIgQJIkqvB9f/ND27YX76IogmVZ2wGquq6jaRqo9H0PTdNWA+I4hkrXdTAM47sNSLMsw5yVLUxxbduCiCApimI1eDOgrmuoVFX18b7nedObYRggyfP8t4AwDDGOIyREBMdx3t4vyxKu624GPDktAwiEwSAKqyBJBYEQRYooFFUApAAIRAmCVAkEKFAQqqIAQAAIAAgCKVCASEGogpDi5cH8M6utx7HurvW13b3NZrMRluf+DRCNRrFcLiFqPB4regOBADabDWdHFcBgMKBcLuN6vfJKIp/P/waIRCLI5XIQdb/f4XA4ZL2j0QilUolzoArQbDbBq7nb7WA2m5nTBsDm0+kEUfV6XeojzH6/h9VqVQXw+/14Pp+gGo0Gc9oBeNxutyGK024ymcBatVpFr9fjsSpAv9+XcvF4XD+Ay+WSnZjKZDIgBDfF6/V+BRA9ZTgc8g8xtAMwZrMZKHHH0+k05vM566oAzD0eD2mLEokEgsEgQx9AMpmUreT7/cZ6vUYqlfoKQGt/vV6g+H2fz6fvFohrtFqtIGq73cJoNH4FYJ2rR1G1Wu0/AEaxWISoSqUi1NVnYLFYSLnj8Qin0/kfgMViwfl8BnW73WC32zUBcG1F0bTC4bB+AEan0wE1GAz4WRMA7fdwOEAQ50EdgI9QrlehUFDU3G43f4Tmoqh5PB4Op2xGaM+sxWIxXC4XiPr5QtLtdhEKhRQ92WxWkaNXtFotTCYTMej/fCGR4KfTKZ2Tt1AE+IxOGJGjYCXpwDdKHwygAx4OeMdkILtm75A7qfYgATr3C+0Z0IAsNEge0rB7/gC9ew4APpg+MyQA+4AAAAAASUVORK5CYII=)
    
    Leejjon
    
    
    
    ](https://leejjon.medium.com/streaming-with-remix-on-google-cloud-platform-app-engine-flex-cloud-run-4e3e16b8c68d#:~:text=App%20Engine%20Flexible%20is%20a,Engine%20Standard%20for%20this%20reason.)
    
- [
    
    Choose an App Engine environment - Google Cloud
    
    Compare the flexible environment to Compute Engine. The App Engine flexible environment has the following differences to Compute E...
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAACjUlEQVR4AWKgBIyCV86mHCBMZ0tNALTVQ4AdQRSF4WCwiW3btm3btr2JzW1s27btLLPJ2OxodPPXGFXDzuJ7fnXObXYidAXO4EqsM1ihvvtfk5aJDf0OSQO/abRE/ceu8Da4hwhIOkXgHtpkZVM7sUA//IFklGvn1nJs9NqwDuutfh3WWU6ZmbwHXCCZcXjsRum9ykMo4IIemdnnPhADCx/YSvcU9RpW3OSEq+DEfFAmveEO3h0bb0sl/BFGeHdoVAkFYlVSn+FRosmTWmdt49khPQWa+XRu5OI3pLYETK4qQXMqSvDi8hI4o7IEzqz07PfBfOXC7znmMF0X+q1020WQBUnGBc3SLBAwrvqy0PUl5M/J3BJ2w1kIixZ2N5ofrx9gnun/TFoE51SoxjJjcNg9BycW7hF22ylIBaaBMg63eK6jLcH+NmwFH/TQnhUqHC6QDHiDfIYS9zQF9GcFi5SBDySD3rDlihgKrEocbDwrWMSBRbZlJhz11BqGApMShxrPChapwf78pgmwcAFNUA1j+N0r0+SaAvnQAhdgaQp867A+tIYq0IPFLE2BCwQWSHag1uKze4bJDWdFaIHYEpKMhR6qwBCIRgu77qaxW0I0hhgLqGltK7DOqmUswCYdZNgC45DDhulzYJzhQByktkAH+GkKvEIdGwrUwStIUqF+6KAOrCIE3Ute4C+X3nc3i1qNTg3ch1VaJ4ZvUOe7WegOnkMgGvfUZTvuWjAveYFPNwvL8LOdhKBUsVBmJb2fqGt73OQqvNPpXsZQGwrc0t0L6uDNZ/PkdhV4A/2xRYF8vc90P9Hw1EA/+wuog846gnypHrWE50EHFj8FLxsKeOGUOuLxb3zo9o2CUQAAQTP7qwJoUEkAAAAASUVORK5CYII=)
    
    Google Cloud
    
    
    
    ](https://cloud.google.com/appengine/docs/the-appengine-environments#:~:text=of%20the%20environments.-,Compare%20the%20flexible%20environment%20to%20Compute%20Engine,using%20the%20Cloud%20Build%20service.)
    
- Show all
    

Generative AI is experimental.

[](https://policies.google.com/privacy?hl=en)

## Featured snippet from the web

The App Engine flexible environment has the following differences to Compute Engine: **The flexible environment VM instances are restarted on a weekly basis**. During restarts, Google's management services apply any necessary operating system and security updates. You always have root access to Compute Engine VM instances.