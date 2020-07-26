<properties
	pageTitle="Problem provisioning or managing workspace"
	description="Problem provisioning or managing workspace"
	infoBubbleText="Problem provisioning or managing workspace"
	service="microsoft.machinelearning.workspace"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32690836"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.workspace.manage"
	ownershipId="AzureML_AzureMachineLearningServices"
/>


# Problem provisioning or managing workspace
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Problem provisioning or managing workspace",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "client",
            "order": 1,
            "controlType": "radiobuttongroup",
            "displayLabel": "Which client are you using?",
            "radioButtonOptions": [
                {
                    "value": "Azure Portal or ML Studio UI",
                    "text": "Azure Portal or ML Studio UI"
                },
                {
                    "value": "Python SDK",
                    "text": "Python SDK"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "REST API",
                    "text": "REST API"
                }
                {
                    "value": "ARM Template",
                    "text": "ARM Template"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "version",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "If applicable, what SDK/CLI/API version are you using?",
            "required": false
        },
        {
            "id": "description",
            "order": 3,
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
