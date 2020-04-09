<properties
	pageTitle="CloudServices RCA"
	description="MachineKey Update Insight"
	infoBubbleText="Found information related to Machine Key Status. See details on the right."
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="mmccrory"
	displayOrder=""
	articleId="MachineKey_NeedsMitigation"
    diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_CloudServices_Content"
/>
# We ran diagnostics on your resource and found an issue

As of <!--$LastRefreshTime-->LastRefreshTime<!--/$LastRefreshTime-->, **<!--$DeploymentName-->DeploymentName<!--/$DeploymentName-->** is not using the enhanced algorithm to encrypt your machine key. Unless you have redeployed or deleted your Cloud Service deployments since <!--$LastRefreshTime-->LastRefreshTime<!--/$LastRefreshTime-->, this status is likely correct.

To use the enhanced algorithm, perform the steps provided in this [advisory](https://aka.ms/azuremachinekeyinfo). You can also check this [advisory](https://aka.ms/azuremachinekeyinfo) for directions to identify if your deployments are using the enhanced algorithm.

If there are any additional Cloud Service deployments under your subscription, they will be listed down here with their current MachineKey status as of <!--$LastRefreshTime-->LastRefreshTime<!--/$LastRefreshTime-->:
## List of Azure Cloud Service deployments
<!--$DeploymentList-->DeploymentList<!--/$DeploymentList-->