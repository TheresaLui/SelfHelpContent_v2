<properties
pageTitle="Top common problems for resource groups"
description="Menu based workflow document for top compute problems"
service="microsoft.compute"
resource="virtualmachines"
authors="summertgu"
ms.author="tiag"
displayOrder=""
articleId="resourcegroupdns"
selfHelpType="diagnoseandsolve"
# resourceTags="windows, linux, ubuntu, redhat, suse"
productPesIds="14749, 15571"
cloudEnvironments="public, Fairfax, usnat, ussec"
ownershipId="Compute_VirtualMachines_Content"
/>
# Diagnose and solve v2 test article for windows
---
{
  "$schema": "SelfHelpContent",
  "commonProblems": [
	{					   
      "id": "Troubleshoot_Deployment_Failures",
      "title": "Troubleshoot Deployment Failures",
      "description": "Troubleshoot failures and errors when creating a new VM in Azure",
      "category": "Virtual Machines",
      "searchTags": "create, image, deploy, deployment, start, quota, size, snapshot, provision, capture, vhd, resource, subscription, time, ARM, network, server, SQL, marketplace, extension, standard, network, operation",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Allocation_failure",
          "title": "Allocation failure",
          "description": "Troubleshoot allocation failures when creating a new VM in Azure",
          "supportTopicId": "32628252",
          "commonSolutionArticleId": "9c0b9ec9-a07a-40e3-a6a2-f4d49f5f4ccb",
          "symptomId": ""
        },
        {
          "id": "Captured_or_generalized_image_deployment_failure",
          "title": "Captured or generalized image deployment failure",
          "description": "Troubleshoot issues when creating a managed image of a generalized VM in Azure",
          "supportTopicId": "32628259",
          "commonSolutionArticleId": "759ac937-32e7-4e89-a82c-28287ad85f9e",
          "symptomId": ""
        },
        {
          "id": "Provisioning_or_deployment_timeout_error",
	  "title": "Provisioning or deployment timeout error",
          "description": "Troubleshoot provisioning or deployment timeout errors when creating a new VM in Azure",
          "supportTopicId": "32628279",
          "commonSolutionArticleId": "2b6deeb3-490a-4d18-8a36-83ed65de8451",
          "symptomId": ""
        },
        {
          "id": "ARM_template_error",
          "title": "ARM template error",
          "description": "Troubleshoot issues when deploying with ARM template",
          "supportTopicId": "32628255",
          "commonSolutionArticleId": "91c00640-5896-42ec-9b42-652a3143fd0d",
          "symptomId": ""
        },
        {
          "id": "Custom_image_deployment_failure",
          "title": "Custom image deployment failure",
          "description": "Troubleshoot issues when deploying a custom image",
          "supportTopicId": "32628262",
          "commonSolutionArticleId": "69867902-65a9-4c5a-aa04-91c748bd351d",
          "symptomId": ""
        },
        {
          "id": "Marketplace_image_deployment_failure",
          "title": "Marketplace image deployment failure",
          "description": "Troubleshoot issues when deploying a marketplace image",
          "supportTopicId": "32628274",
          "commonSolutionArticleId": "0bb36f17-2342-4c60-8bcd-e4416a54a9cd",
          "symptomId": ""
        }
      ]
    },
		{
			"id": "Allocation_recommender",
			"title": "Allocation Success Recommender",
			"description": "Provide prediction of the chance of a successful allocation in the next 7 days for given sizes and regions.",
			"category": "Virtual Machines",
			"searchTags": "deploy, deployment, create, allocation, standard, resource, size, region, available, location, instance",
			"supportTopicId": "32743100",
			"commonSolutionArticleId": "37f0fdfb-3b67-4b90-b692-c0db770af827",
			"symptomId": ""
		},
		{
      "id": "VM_Deployment_Guidance",
      "title": "VM Deployment Guidance",
      "description": "Guidance on creating a new VM in Azure",
      "category": "Virtual Machines",
      "searchTags": "deploy, deployment, create, disk, manage, network, image, vhd, server, standard, resource, size, region, available, location",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Deploy_with_managed_disks",
          "title": "Deploy with managed disks",
          "description": "Guidance on deploying with managed disks or converting a VM from unmanaged disks to managed disks",
          "supportTopicId": "32628271",
          "commonSolutionArticleId": "f29b946f-107f-4c9d-8574-0014f3c2b8f6",
          "symptomId": ""
        },
        {
          "id": "Prepare_an_image",
          "title": "Prepare an image",
          "description": "Guidance on capturing a VM to image in Azure",
          "supportTopicId": "32628272",
          "commonSolutionArticleId": "a316fb37-cb8c-4b94-bdb1-276b2d90a555",
          "symptomId": ""
        },
        {
          "id": "Choosing_Region_or_VM_size",
          "title": "Choosing Region or VM size",
          "description": "Guidance on creating a new VM in an unavailable size or region, or when finding suitable SKU for deployment",
          "supportTopicId": "32628263",
          "commonSolutionArticleId": "37f0fdfb-3b67-4b90-b692-c0db770af827",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "Allocation_failure_Top",
      "title": "Allocation failure",
      "description": "Troubleshoot allocation failures with a VM in Azure (Start VM or Create VM)",
      "category": "Virtual Machines",
      "searchTags": "allocation",
      "supportTopicId": "32628252",
      "commonSolutionArticleId": "9c0b9ec9-a07a-40e3-a6a2-f4d49f5f4ccb",
      "symptomId": ""
    }
  ]
}
---
