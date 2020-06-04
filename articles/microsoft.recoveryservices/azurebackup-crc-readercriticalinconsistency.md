<properties
    pageTitle="ReaderCriticalInconsistency"
    description="ReaderCriticalInconsistency"
    infoBubbleText="We have identified that your backup operation is failing due to USN backup failures"
    service="microsoft.recoveryservices"
    resource="backup"
    authors="srinathvasireddy"
    ms.author="srinathvasireddy"
    displayOrder=""
    articleId="azurebackup-crc-readercriticalinconsistency"
    diagnosticScenario="azurebackup-crc-readercriticalinconsistency"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>


# Error ReaderCriticalInconsistency

<!--issueDescription-->
We have identified that your backup operation is failing due to USN backup failures.
<!--/issueDescription-->

## **Recommended Step**

 To resolve this issue, ensure any protected folder that is deleted and recreated with the same name is not a root directory.  However it can be a sub-directory inside the protected directory.

- For example:  A directory **abc** is the root directory that is protected and is deleted and recreated with the same name. In this case this directory **abc** should be moved inside any directory **xyz** and the policy must be changed to protected **xyz**. 

 
