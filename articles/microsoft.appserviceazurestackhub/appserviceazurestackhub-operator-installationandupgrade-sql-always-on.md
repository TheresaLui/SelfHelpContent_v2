<properties
    pageTitle="App Service operator installation and upgrade SQL Always On"
    description="App Service operator installation and upgrade SQL Always On"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="BryanLa"
    ms.author="bryanla"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32742870"
    resourceTags=""
    productPesIds="17136"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="appserviceazurestackhub-operator-installationandupgrade-sql-always-on"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# App Service operator installation and upgrade SQL Always On

## **Recommended Steps**

SQL Server instances must be accessible from all App Service roles, as well as the App Service resource provider (RP) blade in the administrator portal.

### 1. Verify completion of prerequisites and post-deployment steps

Confirm that you've followed the [deployment prerequisites](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started), and [post-deployment steps](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-deploy?pivots=state-connected#post-deployment-steps), specifically:

- If you deployed using your own SQL Server instance (ie: did NOT use the [Quickstart template for Highly Available file server and SQL Server](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started#quickstart-template-for-highly-available-file-server-and-sql-server)), review [Prepare the SQL Server instance](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started#prepare-the-sql-server-instance) to ensure your SQL Server is deployed in a highly available configuration and configured correctly. 

- For production deployments, SQL Server must also be configured to be highly available and capable of handling failures, using the SQL Always On feature. Following deployment of the App Service resource provider, you must also [add the appservice_hosting and appservice_metering databases to an Always On availability group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-add-a-database), and synchronize the databases to prevent any loss of service in the event of a database failover. 

### 2. Verify that SQL Server is reachable from the App Service RP blade

If you deployed SQL Server using the "Quickstart template for Highly Available file server and SQL Server", you can attempt to restart the SQL Server instances deployed. First you remote into one of the App Service controller VMs, then into each SQL Server VM:

1. Sign in to the Azure Stack Hub administrator portal. Open the App Service RP blade. If you see a raining cloud image with text *"Failed to load App Service extension. Please check whether App Service resource provider and sql database is up and running"*, the database is not reachable. Continue with the following steps.
2. Get the IP addresses for the SQL Server load balancer and the SQL Server database VMs. You'll use them in later steps:
    1. Open the "Virtual machines" service. 
    2. Open the SQL Server VMs (APS-SQL-0 and APS-SQL-1) and note their "Private IP" address properties.
    3. Open the "Resource groups" service.
    4. Select the "AppService.local" resource group, then select "Deployments" in the left pane.
    5. Enter "Microsoft.Template" in the filter text box, and select the "Microsoft.Template" entry in the list.
    6. Select "Outputs" in the left pane. Note the "sqLserver" IP address property to the right.  
3. Establish a remote desktop connection with one of the App Service controller VMs:
    1. Open the "Network security groups" service, and select the "ControllersNsg" group.
    2. Under "Inbound security rules", add/allow an inbound port rule for RDP, port 3389.
    3. Open the "Virtual machines" service again, and select the CN0-VM or CN1-VM controller VM (either will work).
    4. Select "Connect" at the top of the controller VM blade. You'll need the admin credentials provided during deployment to sign in.
4. From the controller VM, verify whether any database node(s) are not reachable:
    1. Find and run the "Web Cloud Management Console" app. You can find a link on the Start menu or desktop, or using search.
    2. In the left pane of the "Web Cloud Management Console" app, select the "Databases" node.
    3. If you see 4 databases show in the "Databases" center pane, each of them is reachable by the App Service controllers, and you can skip to step #8 below. Otherwise, continue with the next step to restart the database instances.

5. From the controller VM, verify connectivity with the SQL Server load balancer and database instances, restarting the SQL Server database instances if necessary:
    1. Use the Start menu to find and run the "Remote Desktop Connection" app. 
    2. Use one of the SQL Server IP addresses obtained in step 2.ii to connect to that SQL Server VM. You'll need the admin credentials provided during deployment to sign in.
    3. In the SQL Server VM, select and run "SQL Server Management Studio" from the Start menu. When the "Connect to Server" dialog shows, make sure "Server type" is set to "Database server", and "Authentication" is set to "Windows Authentication".
    4. First test for connectivity to the SQL Server load balancer, by entering the IP address obtained in step 2.vi in the "Server name" field.  Select the "Connect" button. If login fails and you cannot connect to the SQL Server load balancer, jump to step #7 so you can proceed with opening a support case.
    5. Now test for connectivity to each SQL Server VM's databases.
        1. In the "Object Explorer" panel, select the "Connect" dropdown, then "Database Engine".
        2. In the "Connect to Server" dialog, enter a SQL Server VM IP address from step 2.ii under "Server name". 
        3. Select the "Connect" button. If login fails and you cannot connect to the SQL Server database, jump to step #7 so you can proceed with opening a support case. 
        4. After a successful connection, right-click on the topmost SQL Server node just added to the "Object explorer" panel (begins with its IP address). Select "Restart", then select "Yes" to confirm the *"Are you sure you want to restart the MSSQLSERVER service"* message. Wait for the successive *"Attempting to stop"* and **"Attempting to start"* dialogs to complete.
        5. In the "Object explorer" panel, expand the "Databases" node under the parent SQL Server node, and verify that the "appservice_hosting" and "appservice_metering" databases are "Synchronized". 
        6. Repeat step #6 until you've tested both SQL Server VM's IP addresses.
6. If you got this far, you were able to successfully connect to the SQL Server load balancer and both VMs, and restart the SQL Server databases on both VMs.
7. Close the remote desktop session with the SQL Server VM. 
8. Close the remote desktop session with the controller VM. 
9. Return to the "Network security groups" service in the Azure Stack Hub administrator portal. Delete/deny the "ControllersNsg" group RDP port opened previously in step 3.
10. Return to the App Service RP blade in the and verify that the database is now reachable. If the database is still not reachable, proceed with opening a support case to contact a support engineer.

If you provided your own SQL Server databases during deployment, you'll need to complete similar steps or additional diagnosis to verify that your SQL Server instances are running and reachable.

### 3. Verify that you're using the correct SQL Server SA password

If an SA password was changed from what it was when you deployed, this can also prevent SQL Server from being reachable. If this is the cases,  proceed with opening a support case to contact a support engineer for resolution.

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)

