<properties
	pageTitle="Scoping questions for Moving resources"
	description="Moving resources"
	service="microsoft.web"
	authors="shrahman"
	selfHelpType="supportTopicBasedScopingQuestions"
	supportTopicIds="32581619"
	productPesIds="14748"
	cloudEnvironments="public"
/>

# Moving resources
* Are you moving App Service resources in the same subscription; i.e. from one resource group to another, or from one subscription to another one? 
* What is the combination of resources you are trying to move? Is it just App Services or are App Service Plans involved as well? 
* How many resources are you trying to move? 
* Do any of the App Services have SSL certificates configured on them? Have you uploaded SSL certificates or App Service Certificates? 
* Does the destination resource group have any App Service resources in it? 