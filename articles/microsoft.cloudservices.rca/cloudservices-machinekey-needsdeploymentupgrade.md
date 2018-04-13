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
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

**<!--$DeploymentName-->DeploymentName<!--/$DeploymentName-->** is not using the latest guest agent version. Please perform an [upgrade deployment](https://msdn.microsoft.com/en-us/library/azure/ee460793.aspx) so **<!--$DeploymentName-->DeploymentName<!--/$DeploymentName-->** will be on the latest guest agent, and we determine if your web roles are using the enhanced algorithm.