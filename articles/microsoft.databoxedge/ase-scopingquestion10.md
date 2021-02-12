<properties
	pageTitle="Scoping Questions for Azure Stack Edge VMs"
	description="Scoping Questions for Azure Stack Edge VMs"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32780684, 32780678, 32780683, 32780680, 32780679, 32780677, 32780681, 32780685"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="SharesScopingQuesASEVMs"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box Edge issues with VMs
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Stack Edge issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the problem first observed?",
            "required": true
        },
	{
	     "id": "VM Type",
	     "order": 200,
	     "controlType": "dropdown",
	     "displayLabel": "Which VM do you plan to or have deployed",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Windows VM",
                    "text": "Windows VM"
                },
                {
                    "value": "Linux VM",
                    "text": "Linux VM"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
	    ],
            "required": true
        },
        {
	     "id": "VM Deployment",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "How do you plan to or have deployed VM?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Via Templates",
                    "text": "Via Templates"
                },
                {
                    "value": "Azure Powershell",
                    "text": "Azure Powershell"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
		{
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
	    ],
            "required": true
        },
	{
	     "id": "VM Source Image",
	     "order": 400,
	     "controlType": "dropdown",
	     "displayLabel": "From where do you plan to deploy VM image",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Marketplace image",
                    "text": "Marketplace image"
                },
                {
                    "value": "Own custom image",
                    "text": "Own custom image"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
	    ],
            "required": true
        },
	{
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details regarding the issue, such as Error that you are getting.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox-online/azure-stack-edge-gpu-deploy-virtual-machine-templates'>Learn more</a> about Azure Stack Edge VM Deployment and management"
        }
	],
	"$schema": "SelfHelpContent"
}
---
