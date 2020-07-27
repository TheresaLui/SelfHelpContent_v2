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
    schemaVersion="1"
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
