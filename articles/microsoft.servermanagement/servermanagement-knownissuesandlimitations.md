<properties
	pageTitle="Known issues and limitations"
	description="Known issues and limitations with Server management tools"
	service="microsoft.servermanagement"
	resource="nodes"
	authors="jol"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Known issues and limitations
* Nano Server<br>
Online domain join and online change in workgroup membership of Nano servers is not supported. See [Getting Started with Nano Server](https://technet.microsoft.com/en-us/library/mt126167.aspx) or [Nano Server Domain Join (Deployment-at-a-scale an introduction)](https://blogs.technet.microsoft.com/privatecloud/2016/05/02/nano-server-domain-join-deployment-at-a-scale-part-1-introduction/) for instructions on joining Nano Server to a domain.
* Registry Editor<br>
Editing Binary values is not supported.
* Services<br>
Any action taken on a service, such as Start or Stop service, will be reflected in the UI after 10 seconds.
