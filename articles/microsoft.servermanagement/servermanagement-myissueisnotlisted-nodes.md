<properties
	pageTitle="My issue is not listed"
	description="My issue is not listed"
	service="microsoft.servermanagement"
	resource="nodes"
	authors="jol"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	issueNotListed="true"
/>

# My issue is not listed
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
Please reach out to us if you run into any problems or have feedback on Server management tools!
* Send feature requests or bug reports to [UserVoice](https://aka.ms/smt-engage)
* Connect with [@servermgmt](https://twitter.com/servermgmt) on Twitter and send us comments or questions
* Visit our [blog](https://aka.ms/smt-blog) for news, updates and documentation