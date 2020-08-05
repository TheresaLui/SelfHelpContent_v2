<properties
	pageTitle="Docker, Kubernetes, HELM, ACR deployments"
	description="Azure Pipelines issues related to deploying to Docker, Kubernetes, Helm or ACR deployments"
	infoBubbleText="Azure Pipelines issues related to deploying to Docker, Kubernetes, Helm or ACR deployments"
	service="microsoft.visualstudio"
	resource="account"
	authors="anraghun"
	ms.author="anraghun"
	articleId="AZDevOpsPipelinesContainerDeploymentIssues"
	supportTopicIds="32742310"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines issues related to deploying to Docker, Kubernetes, Helm or ACR deployments

## **Recommended Steps**

Are you facing one of these common problems?

* HelmDeploy task throws error **'unknown flag: --wait'** while running 'helm init --wait --client-only' on Helm 3.0.2 version

    Helm 3 has removed tiller and hence `helm init` command is no longer supported. Remove command: init when you use Helm 3.0+ versions.

* When using Helm 3, if **System.debug is set to true** and Helm upgrade is the command being used, the pipeline fails even though the upgrade was successful

    This is a known issue with Helm 3, as it writes some logs to stderr. Helm Deploy Task is marked as failed if there are logs to stderr or exit code is non-zero. Set the task input **failOnStderr: false** to ignore the logs printed to stderr.

* My Kubernetes cluster is behind a firewall and I am using hosted agents. How can I deploy to this cluster?

    You can grant hosted agents access through your firewall by allowing the IP addresses for the hosted agents. For more details, see [Agent IP ranges](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops&tabs=yaml#agent-ip-ranges)

* HelmInstaller task running on a private agent behind a proxy fails to download helm package

    The HelmInstaller task does not use the proxy settings to download the file https://get.helm.sh/helm-v3.1.0-linux-amd64.zip. You can work around this by pre-installing Helm on your private agents.

* While creating ARM or Kubernetes service connections, I am unable to see the list of Azure subscriptions I have access to

    If you don't see any Azure subscriptions or instances, or you have problems validating the connection, see [Troubleshoot Azure Resource Manager service connections](https://github.com/MicrosoftDocs/azure-devops-docs/blob/master/docs/pipelines/release/azure-rm-endpoint.md).

* Docker build command fails with **No Dockerfile matching \<path-to-dockerfile\> was found**

    Provide absolute repo path to the dockerfile

## **Recommended Documents**

* [Troubleshoot Azure Resource Manager service connections](https://github.com/MicrosoftDocs/azure-devops-docs/blob/master/docs/pipelines/release/azure-rm-endpoint.md)
* [Build and push Docker images](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/docker?view=azure-devops)
* [Deploy to Kubernetes using Helm](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/helm-deploy?view=azure-devops)
* [Deploy to Kubernetes using Kubectl](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/kubernetes?view=azure-devops)