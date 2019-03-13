<properties
    pageTitle="Azure Stack Deployment Questions"
    description="Azure Stack Deployment Questions"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629176,32629205"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-deploymentandregistration-deployquestions"
/>

# Azure Stack deployment worksheet

If you’re interested in an Azure Stack integrated system, you should understand some of the major planning considerations around deployment and how the system fits into your datacenter.<br>

You can find guidance about planning for hosting Azure Stack in the [Datacenter integration considerations for Azure Stack integrated systems] article. The article also includes the the [Azure Stack capacity planner spreadsheet](https://aka.ms/azstackcapacityplanner).<br>

To deploy Azure Stack, you need to provide planning information to your solution provider before deployment starts to help the process go quickly and smoothly. The information required ranges across networking, security, and identity information with many important decisions that may require knowledge from many different areas and decision makers.<br>

The Azure Stack capacity planner spreadsheet helps you make informed decisions with respect to planning capacity in two ways: either the by selecting a hardware offering and attempting to fit a combination of resources or by defining the workload that Azure Stack is intended to run to view the available hardware SKUs that can support it. Finally, the spreadsheet is intended as a guide to help in making decisions related to Azure Stack planning and configuration.<br>


## **Recommended steps**

1. Provide planning information to your solution provider.<br>
2. Pull in people from multiple teams in your organization to ensure that you have all required information ready before deployment begins.<br>
3. Talk to your hardware vendor while collecting this information. <br>
4. Make some pre-deployment configuration changes to your network environment. <br>
5. Line up subject area experts to help you with your planning.<br>
6. Use the [Azure Stack capacity planner spreadsheet](https://aka.ms/azstackcapacityplanner) to help you make informed decisions with respect to planning capacity.<br>
7. Review the worksheets [contained in the planner](https://docs.microsoft.com/azure/azure-stack/capacity-planning-spreadsheet).<br>
8. The **DefinedSolutionSKUs** worksheet contains up to five hardware definition examples. Change details to match the system configurations being considered for use or purchase. For instructions, see [DefinedSolutionSKUs instructions](https://docs.microsoft.com/azure/azure-stack/capacity-planning-spreadsheet#definedsolutionskus-instructions).<br>
9. Create a model using a single collection of various sizes and quantities of VMs, select the **DefineByVMFootprint** tab and follow this sequence of steps in the [DefineByVMFootprint instructions](https://docs.microsoft.com/azure/azure-stack/capacity-planning-spreadsheet#definebyvmfootprint-instructions).<br>
10. Create a model using a collection of Azure Stack Workloads, select the **DefineByWorkloadFootprint** tab and follow the [DefineByWorkloadFootprint instructions](https://docs.microsoft.com/azure/azure-stack/capacity-planning-spreadsheet#definebyworkloadfootprint-instructions). Azure Stack Workloads are created using available VM resources.<br> 

## **Recommended documents**

[Azure Stack deployment connection models](https://docs.microsoft.com/azure/azure-stack/azure-stack-connection-models)<br>
[Azure connected Azure Stack deployment decisions](https://docs.microsoft.com/azure/azure-stack/azure-stack-connected-deployment)<br>
[Azure disconnected Azure Stack deployment decisions](https://docs.microsoft.com/azure/azure-stack/azure-stack-connection-models)