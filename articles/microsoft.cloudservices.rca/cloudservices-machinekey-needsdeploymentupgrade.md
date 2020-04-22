<properties
	pageTitle="CloudServices RCA"
	description="MachineKey Update Insight"
	infoBubbleText="Found information related to Machine Key Status. See details on the right."
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="mmccrory"
	displayOrder=""
	articleId="MachineKey_NeedsDeploymentUpgrade"
    diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_CloudServices_Content"
/>
# We ran diagnostics on your resource and found an issue

As of <!--$LastRefreshTime-->LastRefreshTime<!--/$LastRefreshTime--> **<!--$DeploymentName-->DeploymentName<!--/$DeploymentName-->** is not using the latest guest agent version. Please perform an [upgrade deployment](https://msdn.microsoft.com/library/azure/ee460793.aspx) so **<!--$DeploymentName-->DeploymentName<!--/$DeploymentName-->** will be on the latest guest agent, and we determine if your web roles are using the enhanced algorithm.

If there are any additional Cloud Service deployments under your subscription, they will be listed down here with their current MachineKey status as of <!--$LastRefreshTime-->LastRefreshTime<!--/$LastRefreshTime-->:
## List of Azure Cloud Service deployments
<!--$DeploymentList-->DeploymentList<!--/$DeploymentList-->