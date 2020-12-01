<properties
	pageTitle="Authentication Issues"
	description="Authentication Issues"
	infoBubbleText="Authentication Issues"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32690837"
	productPesIds="16644"
    schemaVersion="1"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.authentication-scopingq"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Authentication Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Authentication Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "auth_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What type of authentication are you facing issues with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Interactive",
                    "text": "Interactive Authentication"
                },
                {
                    "value": "Service Principal",
                    "text": "Service Principal"
                },
                {
                    "value": "Managed Identity",
                    "text": "Managed Identity"
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
