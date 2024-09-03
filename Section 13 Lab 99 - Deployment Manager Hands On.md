1. Hamburger icon go APIs & Services
2. Enabled API & Services
3. Hamburger icon -API-Dashboard
4. Type "Deployment manager"
5. click - Cloud Deployment manager -Cloud Deployment Manager V2 API-Enable
6. Search box -Deployment manager
7. Deploy marketplace solution (solution already made)
8. Google Cloud shell because we will create our own solution
9. Make sure you're in your project
10. Make directory mkdir deploymentmanager
11. ls to verify its there.
12. Code editor and look for "deploymentmanager"
13. Right click on file above and create new file "sampleconfig.yaml"
14. command promt cd deploymentmanager
15. LS to see if we have the sampleconfig.yaml file
16. create deployment command line gcloud deployment-manager deployments create my-first-deployment --config Sampleconfig.yaml - enter ps use the yaml file provided
17. State:completed
18. When we go to VM instances we can see it's deployed in us-central one. Machine type is n1 Standard 1.
19. The instance my-firstdeployment-vm is being deployed from the deployment manager.
20. Go to console search box again and type "deployment manager" there you'll see configuration,layout and expanded config.
21. Go back to command prompt and try to create same deployment manager. You'll get error 409 already exists
22. change the name of the deployment and create a deployment like my-first-deployment-1
23. describe deployment gcloud deployment-manager deployments describe my-first-deployment
24. delete operations gcloud deployment-manager deployments delete my-first-deployment-4ted. When you delete the duplicate deplooyment it will delete the instance as well.
25.  Make sure not to create common resources in the deployments.
26. Create new deployment first creating a new file under deployment manager. The file is a "jinja" file
27. Copy from name down on the sampleconfig.yaml file and paste this in the net vm-template.jinja file
28. Create a new file "dynamicConfig.yaml " first import imports: - get the absolute path to the vm-template.jinja file which can be obtained with "readlink -e vm-template.jinga"  so it would look like this imports: next line -path: file:///home/claytonted05/deploymentmanager/vm-template.jinja. Correction just put this as the path "vm-template.jinja"