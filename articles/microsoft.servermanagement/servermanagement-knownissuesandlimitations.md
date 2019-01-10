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
	cloudEnvironments="public, MoonCake"
/>

# Known issues and limitations
* Nano Server<br>
Online domain join and online change in workgroup membership of Nano servers is not supported. See below for instructions on joining Nano Server to a domain.<br>
[Getting Started with Nano Server - Joining Nano Server to a domain](https://technet.microsoft.com/en-us/library/mt126167.aspx#Anchor_4)<br>
[Nano Server Domain Join (Deployment-at-a-scale an introduction)](https://blogs.technet.microsoft.com/privatecloud/2016/05/02/nano-server-domain-join-deployment-at-a-scale-part-1-introduction/) 
* Registry Editor<br>
Editing Binary values is not supported.
* Services<br>
Any action taken on a service, such as Start or Stop service, will be reflected in the UI after 10 seconds.
* Certificate Manager<br>
Certificate import and export are not supported on the Nano Server version of Windows Server 2016 Technical Preview (TP) 5. You will get an error that 'CertPKICmdlet.dll' is missing. This will be fixed in the RTM version of Nano Server.
