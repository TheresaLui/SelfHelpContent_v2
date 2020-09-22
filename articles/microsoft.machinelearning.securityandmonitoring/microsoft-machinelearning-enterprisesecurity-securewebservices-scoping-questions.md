<properties
	pageTitle="Secure Web Services"
	description="Secure Web Services"
	infoBubbleText="Secure Web Services "
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32690883"
	productPesIds="16644"
    schemaVersion="1"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.securewebservices.scoping.q"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Secure Web Services
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Secure Web Services",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "deployment_type",
            "order": 1,
            "controlType": "radiobuttongroup",
            "displayLabel": "Where are you deploying your web service?",
            "radioButtonOptions": [
                {
                    "value": "Azure container instance (ACI)",
                    "text": "Azure container instance (ACI)"
                },
                {
                    "value": "Azure kubernetes service (AKS)",
                    "text": "Azure kubernetes service (AKS)"
                }
            ],
            "required": false
        },
        {
            "id": "auth_type",
            "order": 2,
            "controlType": "radiobuttongroup",
            "displayLabel": "What kind of authentication are you using for your web service?",
            "radioButtonOptions": [
                {
                    "value": "Key-based authentication",
                    "text": "Key-based authentication"
                },
                {
                    "value": "Token-based authentication",
                    "text": "Token-based authentication"
                },
                {
                    "value": "No authentication",
                    "text": "No authentication"
                }
            ],
            "required": false
        },
                {
            "id": "cert_type",
            "order": 3,
            "controlType": "radiobuttongroup",
            "displayLabel": "What type of certificate are you using for your web service?",
            "radioButtonOptions": [
                {
                    "value": "Microsoft generated certificate",
                    "text": "Microsoft generated certificate"
                },
                {
                    "value": "Custom certificate",
                    "text": "Custom certificate"
                },
                {
                    "value": "No certificate",
                    "text": "No certificate"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
