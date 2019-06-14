<properties
	pageTitle="UserErrorConnectionToPrimaryReplicaIsNotActive"
	description="UserErrorConnectionToPrimaryReplicaIsNotActive"
	infoBubbleText="The connection to the primary replica is not active."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorconnectiontoprimaryreplicaisnotactive"
	diagnosticScenario="azurebackup-crc-usererrorconnectiontoprimaryreplicaisnotactive"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error UserErrorConnectionToPrimaryReplicaIsNotActive

<!--issueDescription-->
We have identified that backup operation fails due to connection issues with the primary replica.
<!--/issueDescription-->

## **Recommended Steps**
If the backup operation fails with this error, perform the below steps:

* Check the firewall settings to see if the port 5022 (by default) allows communication between the server instances that host primary replica and the secondary replica.
* Check whether the network service account has connect permission to the firewall.
* Retry backup operation.
