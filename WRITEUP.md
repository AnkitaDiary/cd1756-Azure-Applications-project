# Write-up 

## COMPARISON AND ANALYSIS

### VIRTUAL MACHINE
##### Cost
Running the CMS app on a VM can be more expensive because the VM rauns all the time , even if the app is not being used . We also need to oay for stoagre, networking and maintenance of the VM.

##### Scalability
Scaling a VM machine requires more manual task. If the application gets more traffic, we would need to create more VMs or thence the VM size , which takes extra time and configuration

##### Availability
Availability depends on how VM is configured. If only one VM is used the application may go down if VM fails or needs mainaentnace. To impove this , multiple VMs and load balancing would be  required.

##### Workflow 
Using a VM means developers need to manage the server themselves. This needs more operational work.

### APP SERVICE
##### Cost
Azure App Service is a managed platform, so you mainly pay for the service plan you chose. Since Azure manages the infrastructure, it reduces the cost and effort of maintaining servers.

##### Scalability
App service makes scaling much easier. It supports automatic scaling based on traffic or performance.

##### Availability
App service provides built-in  high availability and reliability. Azure manages the infrastructure and helps keep the applications running with minimal downtime.

##### Workflow
Deployment  is very simple in App Service. Developers can deploy directly from GitHub, which I did in this project, and Azure handles updates, server management and monitoring, allowing developers to focus more on building the application.

## CHOOSEN SOLUTION

I chose Azure App Service for deploying the CMS application. It is easier to manage because Azure handles the infrastructure, updates, and scaling. This reduces the amount of manual work required  and allows for the development of apps quickly.


## Assess app changes that would change your decision.

If the application later requires more control over the server environment or system configuration, then using a Virtual Machine might be a better solution.
A VM would allow  full control over the operating system and installed software. In that case, additional setup would also be needed.
