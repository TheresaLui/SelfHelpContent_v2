<properties
	pageTitle="Authentication & Role Based Access (RBAC)"
	description="Authentication & Role Based Access (RBAC)"
	infoBubbleText="Authentication & Role Based Access (RBAC)"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32690837"
	productPesIds="16644"
    schemaVersion="1"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.authentication"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Authentication & Role Based Access (RBAC)
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Authentication & Role Based Access (RBAC)",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "role_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the machine learning role you are facing issues with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Owner",
                    "text": "Owner"
                },
                {
                    "value": "Contributor",
                    "text": "Contributor"
                },
                {
                    "value": "Reader",
                    "text": "Reader"
                },
                {
                    "value": "Custom",
                    "text": "Custom"
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
