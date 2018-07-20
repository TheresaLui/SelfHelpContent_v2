<properties
pageTitle="FileSync broken ghosts"
description="There are broken ghosts on the server endpoint"
infoBubbleText="See details on right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
displayOrder=""
articleId="FileSync_SyncPerItemError_BrokenGhosts"
diagnosticScenario="FileSync broken ghosts"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **File Sync failed to upload <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> files under Server Endpoint '<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->' as they are broken tiered files**

<!--issueDescription-->
Server Endpoint **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->** contains <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> non-functional ("broken") tiered files. These tiered files have been rendered non-functional due to this server endpoint having been deleted without first recalling all the tiered data to the server. These files cannot be synced, and must be deleted. Download the attached script (rename ps_ to .ps1) and follow the instructions in the attached document to remove these broken tiered files.
<br> 
<!--/issueDescription-->
