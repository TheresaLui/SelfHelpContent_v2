<properties
	pageTitle="Data Encryption"
	description="Data Encryption"
	infoBubbleText="Data Encryption"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32740869"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.dataencryption"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Data Encryption
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Data Encryption",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "key_type",
            "order": 1,
            "controlType": "radiobuttongroup",
            "displayLabel": "Are you using Microsoft-managed (default) or customer-managed keys in your machine learning workspace?",
            "radioButtonOptions": [
                {
                    "value": "Microsoft-managed keys",
                    "text": "Microsoft-managed keys"
                },
                {
                    "value": "Customer-managed keys",
                    "text": "Customer-managed keys"
                }
            ],
            "required": false
        },
        {
            "id": "description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "hints": [
                { 
                    "text": "Please describe your issue." 
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
