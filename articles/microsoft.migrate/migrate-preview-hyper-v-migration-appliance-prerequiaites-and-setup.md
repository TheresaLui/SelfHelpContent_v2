<properties
	pageTitle="Migration appliance pre-requisites and setup"
	description="Migration appliance pre-requisites and setup"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631943,32631917"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="ech72d57-c8c4-4009-8d82-f6d50af6c954"
/>

# Migration appliance pre-requisites and setup

## **Recommended Steps**

Hyper-V host validation error: **WinRM cannot process the request or WinRM cannot complete the operation**

Run the following commands on Power shell on the Hyper-V hosts to be discovered:

* `winrm qc`
* `enable-psremoting`

Ensure that port 5985 and 5986 are open on the Hyper-V hosts and clusters added for discovery.
