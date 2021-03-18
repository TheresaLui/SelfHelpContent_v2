<properties
	pageTitle="Environments and Deployment Groups"
	description="Issues related to using environments in a YAML pipeline or deployment groups in a classic release pipelines"
	infoBubbleText="Azure Pipelines issues related to Environments and Deployment groups"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsDeploymentGroupsEnvironments"
	supportTopicIds="32742311"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipeline issues with Environments and Deployment Groups

 
* **The Deployment group agents are offline in Azure DevOps even though I'm able to access the machines through an RDP connection**

    Check if there was any restart of your target machines on which the agents are configured. Ensure after every restart of the target machines that the configured agents are running. Also, make sure they are not running behind a proxy.

* **"Failed to create *Deployment Group Administrators* group for project"**

    Rename the **"Deployment Group Administrators"** group and then try creating a deployment group.

* **"./svc.sh command not found" when creating a Deployment Group on a Linux virtual machine**

    Check the [Linux distributions supported](https://docs.microsoft.com/azure/devops/pipelines/agents/v2-linux?view=azure-devops#check-prerequisites). Ensure the user account that you're using has permission to register the agent. The **./svc.sh** script will run and manage your agent as a **systemd service**. If you [run your agent as a service](https://docs.microsoft.com/azure/devops/pipelines/agents/v2-linux?view=azure-devops#run-as-a-systemd-service), you cannot run the agent service as root user.

* **Unable to configure the Deployment Group agent behind proxy**

    * Set **HTTP_PROXY** and **HTTPS_PROXY** as an environment variable(system variable) with the proxy URL value set to: 
    http://proxyserver:port 
    or  
    https://proxyserver:port
    
    * Restart the server and try to configure the agent again.

* **I cannot register a new target for my Deployment Group**

    Add the user as an Administrator in the **[Deployment pool security policies](https://docs.microsoft.com/azure/devops/pipelines/policies/permissions?view=azure-devops#deployment-pool-security-roles)**.

## **Recommended Documents**

* [Provision agents for deployment groups](https://docs.microsoft.com/azure/devops/pipelines/release/deployment-groups/howto-provision-deployment-group-agents?view=azure-devops)
* [Provision deployment groups](https://docs.microsoft.com/azure/devops/pipelines/release/deployment-groups/?view=azure-devops)
* [Check prerequisites for Linux distributions](https://docs.microsoft.com/azure/devops/pipelines/agents/v2-linux?view=azure-devops#check-prerequisites)
* [Configure an agent behind proxy](https://docs.microsoft.com/azure/devops/pipelines/agents/proxy?view=azure-devops&tabs=windows)
* [Deploy to Azure VMs using deployment groups in Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/release/deployment-groups/deploying-azure-vms-deployment-groups?view=azure-devops)
* [Deployment pool security roles](https://docs.microsoft.com/azure/devops/pipelines/policies/permissions?view=azure-devops#deployment-pool-security-roles)
* [Create and target an environment](https://docs.microsoft.com/azure/devops/pipelines/process/environments?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
