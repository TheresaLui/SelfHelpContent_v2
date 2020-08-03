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

If you deployed SQL Server using the "Quickstart template for Highly Available file server and SQL Server", the SQL Server databases were deployed to Azure Stack Hub as part of the App Service installation. Attempt to restart the SQL Server instances provided during deployment, by remoting into one of the App Service controller VMs, then into each SQL Server VM:

1. Sign in to the Azure Stack Hub administrator portal. Open the App Service RP blade. If you see a raining cloud image with text *"Failed to load App Service extension. Please check whether App Service resource provider and sql database is up and running"*, the database is not reachable. Continue with the following steps.
2. Establish a remote desktop connection with one of the App Service controller VMs:
    1. Open the "Network security groups" service, and select the "ControllersNsg" blade.
    2. Add/enable an inbound security rule for RDP, port 3389.
    3. Open the "Virtual machines" service. Note the "Private IP" addresses for the 2 SQL Server VMs (APS-SQL-0 and APS-SQL-1) as you'll use them later. Then select the CN0-VM or CN-1-VM controller VM (either will work).
    4. Select "Connect" at the top of the controller VM blade. You'll need the admin credentials provided during deployment to sign in.
3. Establish a remote desktop connection with the SQL Server VMs
    1. From the controller VM, use the Start menu to find and run the "Remote Desktop Connection" app. 
    2. Use a SQL Server IP address obtained in step 2.c to connect to the SQL Server VM. You'll need the admin credentials provided during deployment to sign in.
    3. In the SQL Server VM, select and run "SQL Server Management Studio" from the Start menu.
    4. In the "Connect to Server" dialog, enter the name of one of the SQL Server instances (APS-SQL-0 or APS-SQL-1) under "Server name". Leave "Authentication" as "Windows Authentication". Select the "Connect" button.
    5. Using the "Object explorer" panel, right-click on the topmost database server node and select "Restart". Select "Yes" to confirm the "Are you sure you want to restart the MSSQLSERVER service" message. Wait for the "Attempting to stop" and "Attempting to start" dialogs to complete.
    6. In the "Object explorer" panel, expand the "Databases" name and verify that the "appservice_hosting" and "appservice_metering" databases are "Synchronized". 
    7. Click the "Connect" icon (looks like a plug) at the top of the "Object Explorer" panel. Using the name of the second SQL Server instance, repeat steps d through g.
4. Close the remote desktop session with the first SQL Server VM. Using the IP address of the 2nd SQL Server VM, repeat step 3.
5. Close the remote desktop session with the controller VM. Return to the App Service RP blade in the Azure Stack Hub administrator portal and verify that the database is now reachable. 
6. If the database is still not reachable, proceed with opening a support case to contact a support engineer.

If you provided your own SQL Server databases during deployment, you'll need to complete similar steps or additional diagnosis to verify that your SQL Server instances are running.

### 3. Verify that you're using the correct SQL Server SA password

If an SA password was changed from what it was when you deployed, this can also prevent SQL Server from being reachable. You'll need to review log messages to look for clues that would prevent SQL Server from being reachable.

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)

