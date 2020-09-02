<properties
	pageTitle="Virtual Network Configuration"
	description="Virtual Network Configuration"
	infoBubbleText="Virtual Network Configuration"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32740868"
	productPesIds="16644"
    schemaVersion="1"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.virtualnetwork.scoping.q"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Virtual Network Configuration
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Virtual Network Configuration",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "private_link",
            "order": 1,
            "controlType": "radiobuttongroup",
            "displayLabel": "Is your machine learning workspace configured behind a private endpoint?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "associated_resource",
            "order": 2,
            "controlType": "radiobuttongroup",
            "displayLabel": "Are any of your associated resources (storage, container registry, key vault, app insights) configured behind a virtual network or private endpoint?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "single_vnet",
            "order": 3,
            "controlType": "radiobuttongroup",
            "displayLabel": "Are all of your machine learning resources inside the same virtual network?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "architecture",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional network configuration details (if applicable)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
