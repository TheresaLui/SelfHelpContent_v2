<properties
	pageTitle="Scoping Questions for Azure Stack Edge Kubernetes"
	description="Scoping Questions for Azure Stack Edge Kubernetes"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32780673, 32780674, 32780676, 32780675, 32780672, 32780670, 32780671"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="SharesScopingQuesASEK8s"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box Edge issues with Kubernetes
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
	     "id": "IP Settings",
	     "order": 200,
	     "controlType": "dropdown",
	     "displayLabel": "Verify compute network settings, make sure the IPs provided are continuous and not duplicate",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
         	{
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
	    ],
            "required": true
        },
	{
	     "id": "Deployment",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "How do you plan to deploy or have deployed your workload?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Local Deployment",
                    "text": "Local Deployment"
                },
                {
                    "value": "IOT Edge Deployment",
                    "text": "IOT Edge Deployment"
                },
		{
                    "value": "Azure/ARC Deployment",
                    "text": "Azure/ARC Deployment"
                },
         	{
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
	    ],
            "required": true
        },
	{
	     "id": "Management",
	     "order": 400,
	     "controlType": "dropdown",
	     "displayLabel": "How do you plan to manage or how are you managing Kubernetes cluster",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Native tool like Kubectl",
                    "text": "Native tool like Kubectl"
                },
                {
                    "value": "Azure ARC management",
                    "text": "Azure ARC management"
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
            "watermarkText": "Please provide the details regarding the issue, such as the error message that you are receiving.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox-online/azure-stack-edge-gpu-kubernetes-workload-management'>Learn more</a> about Azure Stack Edge Kubernetes workload and management"
        }
	],
	"$schema": "SelfHelpContent"
}
---
