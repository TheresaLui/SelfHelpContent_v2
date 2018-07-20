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

# **File Sync failed to upload <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> broken tiered file(s) for Server Endpoint '<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->'**

<!--issueDescription-->
Server Endpoint **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->** contains <!--$ErrorCount-->[ErrorCount]<!--/$ErrorCount--> broken tiered file(s). These tiered files have been rendered non-functional due to this server endpoint having been deleted without first recalling all the tiered data to the server. These files cannot be synced, and must be deleted. Please use the attached script and instructions to remove these broken tiered files.
<br> 
<!--/issueDescription-->
