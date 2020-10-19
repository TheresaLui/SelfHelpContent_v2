<properties
  pagetitle="Azure Pipelines CLI, REST API, and Web hooks"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="vijayma,whjenkin"
  selfhelptype="Generic"
  supporttopicids="32742295"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesrestapi"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines CLI, REST API, and Web hooks

## **Recommended Steps**

Are you facing one of these common problems?

* I am trying to figure out how to do "X" (replace X with what you are trying to do) using Azure Pipelines APIs. I cannot find documentation or an example to help me.

  The best way for you to see an API in an example is through your browser's **developer tools**. Let us say you are trying to create a pipeline or to run a pipeline using an API. Or, you may be trying to understand how to pass parameters when starting a new run. To understand the structure of the request in each of these cases, simply exercise the same scenario using the browser UI. For instance, create a new pipeline in the Azure Pipelines UI or start a new run with input parameters. If you enable developer tools in your browser as you perform these UI operations, you will be able to see the exact API call that is being made and the entire structure of the request body. This is a good way for you to learn how to use the API.

* I can’t find a list of supported Azure CLI commands or Azure DevOps APIs

  - A complete list of supported commands can be found in the Azure DevOps CLI [getting started documentation](https://docs.microsoft.com/azure/devops/cli/?view=azure-devops)
  - A complete list of supported rest APIs can be found in the Azure DevOps Rest API [docs](https://docs.microsoft.com/rest/api/azure/devops)
  - If command or API needed isn’t listed there, then our service doesn’t currently support it. Please create an item on [developer community](https://developercommunity.visualstudio.com) if you would like to have it supported in the product.

* I’m **unable to authenticate** my REST API call
  
  - Check the Azure DevOps Services REST API [reference](https://docs.microsoft.com/rest/api/azure/devops) to ensure the request is constructed correctly
  - If using a personal access token (PAT), ensure the token has the appropriate scope. The [security section](https://docs.microsoft.com/rest/api/azure/devops/pipelines/pipelines/get#security) of every API doc lists supported auth and required scopes.
  - Ensure the user who is running the action has the right permissions 

* I’m not seeing a **full list of results** on my API call
  
  - Check to see if the API you’re using supports continuation tokens. If so, ensure the token is supplied to your REST call.

* I'm trying to create a webhook
 
  - Check the Azure DevOps Services webhook [guidance](https://docs.microsoft.com/azure/devops/service-hooks/services/webhooks?view=azure-devops) to ensure the webhook is configured correctly

## **Recommended Documents**

* [Azure DevOps CLI](https://docs.microsoft.com/azure/devops/cli/?view=azure-devops)
* [Azure DevOps Rest API](https://docs.microsoft.com/rest/api/azure/devops)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)
* [Azure DevOps Webhooks](https://docs.microsoft.com/azure/devops/service-hooks/services/webhooks?view=azure-devops)
