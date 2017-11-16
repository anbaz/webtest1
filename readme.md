# Create a ICP cluster on OpenPOWER systems cloud 

Beta Service: Please note this is an experimental service and IBM provides no guarantees of availability or preservation of programs or data. 
Use at your own risk.

For IBMers there is a portal service to build ICP 2.1 & 1.2 version on OpenPOWER systems [here] (https://portal1.openpowercontainer.com/dashboard/auth/login)

## Prerequisites
The following tools are required. You need to add these command lines tools accessible from your PATH.
 - Install kubectl CLI
 - [Cmder](https://github.com/cmderdev/cmder) (for Windows environment, you can use Cmder where common Linux tools is included).
 
## Following steps shows how to create ICP Cluster on OpenPOWER systems and access from your workstation or laptop

 - Create your own cluster on OpenPOWER system cloud
 - Setup kubectl to access kubenetes cluster environment from your workstation or laptop
 - Setup service account token for kebectl
 - SSH to cluster environment from your workstation or laptop
 
	
### Create your own cluster on OpenPOWER system cloud

 - Login to portal service using your IBM account [here] (https://portal1.openpowercontainer.com/dashboard/auth/login)
 ![PortalLogin](images/1.PortalLogin.PNG)
 - Enter your IBMid
 ![LoginWithIBMid](images/2_LoginWithIBMid.PNG)
 - Page will be redirected to W3id for authendication if your IBMid associated with IBM W3id
 ![AssociatedWithIBMW3id](images/3.AssociatedWithIBMW3id.PNG)
 - Click on "Launch Container Cluster" icon on the right side of the dashboard.
 ![LaunchContainer](images/4.LaunchContainer.PNG)
 - Pick your ICP version and cluster environment and click on "Launch"
 ![ChooseVersion](images/5.ChooseVersion.PNG)
 - Your cluster will be successfully launched with status as "Create in Progress". Wait for few minitues and refresh your page to see status as "Create Complete". 
   Click on cluster name to access details.
 ![Launched_Create_In_Progress](images/7.Launched_Create_In_Progress.PNG)
 - Cluster Overview tab will provides details about your new cluster and "Access Instructions" tab will guide you to setup kubectl and SSH access.
 ![Cluster_Overview](images/10.Cluster_Overview.PNG)
 ![AccessInformation](images/11.AccessInformation.PNG)
 - Click on console link provided in the access instrctions tab to get into the ICP console
 ![LoginPage_ICP](images/11.LoginPage_ICP.PNG)
 ![Dashboard](images/12.Dashboard.PNG)
 
### Setup kubectl to access kubenetes cluster environment from your workstation or laptop

 - On the ICP dashboard right top corner, click on "admin" icon to get "Configure client" 
 ![ClientConfig](images/13.ClientConfig.PNG)
 - To configure kubectl copy and paste in your terminal windows.
 ![kubectl_details](images/14.kubectl_details.PNG)
 as shown below
 ![kebectl_cmd](images/15.kebectl_cmd.PNG)
 to verify run "kubectl cluster-info" command
 ![kebectl_verification](images/16.kebectl_verification.PNG)
 
 ### Setup service account token for kebectl
 
 - Follow the instrctions on "Access instrctions" tab to setup service account token
   Cmder (preferable for windows) 
 ![Serviceaccountinfo](images/18.Serviceaccountinfo.PNG)
 as shown below
 ![serviceaccount](images/19.serviceaccount.PNG)
 Note: Use printf instead of echo to decode token and then pass the decoded value to configure as shown below
 ![serviceaccountconfig](images/20.serviceaccountconfig.PNG)
 to verify run "kubectl cluster-info" command
 ![kebectl_verification](images/16.kebectl_verification.PNG)
 
 ### SSH to cluster environment from your workstation or laptop
 
 - Follow the instrctions on "Access instrctions" tab to setup SSH session to cluster.
   Open Cmder (preferable for windows)
 ![ToSSH](images/17.ToSSH.PNG)
 as shown below
 ![ssh_login](images/18.ssh_login.PNG)
 