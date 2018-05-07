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
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--$DeploymentName-->DeploymentName<!--/$DeploymentName--> is not using the enhanced algorithm to encrypt your machine key. Please perform the steps provided in this [advisory](https://aka.ms/azuremachinekeyinfo).