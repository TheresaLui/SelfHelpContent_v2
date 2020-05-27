<properties
	pageTitle="Availability/Function App restarted"
	description="Availability/Function App restarted"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,cts-shrahman"
    ms.author="shrahman, onrazvan"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630467"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="67228d28-9e42-46b5-a27a-d89c85cf8552"
	ownershipId="Compute_AppService"
/>

#  Availability/Function App restarted

## **Recommended Steps**

Besides the manual restart you can perform from the Portal, your Function App can restart after performing the following actions:<br>

1. Modifying the host.json or function.json manually from Portal, Kudu, FTP or via App Service Editor will restart the Function App host in order for the new values to be loaded.<br>
2. Adding/Removing Application Settings (environment variables) will restart the Function App since the main process (w3wp.exe) needs to be recycled for the new environment variables to be loaded so your functions can use them.
<br>

**Additional Check**

1. If you have Application Insights, you can check if your Function App was restarted due to modifying files used by your functions using the following query:<br>

   ```
    traces
	| where message == "Host configuration has changed. Signaling restart" or message contains "File change of type 'Changed' detected"
    | order by timestamp desc
   ```

2. Any modifications done to Application Settings (adding variables or removing them) are tracked in the Activity Logs which can be found under Platform features – Resource management. In the Activity Logs, these modifications will be shown as ‘Update web sites config’ operations. If these types of operations are found in your logs, then at that timeframe your Function App was restarted for the new application settings values to be loaded.
