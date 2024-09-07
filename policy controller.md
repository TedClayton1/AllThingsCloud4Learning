

The Anthos Policy Controller is ==a tool that helps enforce policies for Kubernetes clusters==:  

- How it works
    
    The Policy Controller uses constraint objects to enforce policies on a cluster. When a constraint is installed, requests to the API server are checked against the constraint and rejected if they don't comply.  
    
- How to create policies
    
    You can create policies by using constraint templates, which define the policy's schema and logic. You can source constraint templates from Google or third parties, or you can write your own.  
    
- How to monitor policies
    
    The Policy Controller Dashboard provides a centralized view of policy violations, and can suggest how to fix problems. You can also view information about violations, including the recommended action to resolve them.  
    
- How to create the dashboard
    
    To create the Policy Controller dashboard, you can:  
    
    1. Go to the Dashboards page in the Google Cloud console  
        
    2. Click the Sample library tab  
        
    3. Select Anthos Config Management in the Categories column  
        
    4. Select the Policy Controller checkbox in the Anthos Config Management samples table  
        
    5. Click Download Import  
        
    6. Click Confirm in the confirmation window