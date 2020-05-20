<properties
pageTitle="Management Issues"
description="Management Issues"
service="microsoft.containerregistry"
authors="nathana1"
ms.author="nathana"
selfHelpType="problemScopingQuestions"
supportTopicIds="32680720,32680718,32680719,32680721,32680722,32680731"
productPesIds="16213"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="problemscoping-management"
schemaVersion="1"
	ownershipId="ContainerRegistry_Runtime"
/>
# Management Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Management Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "required": true,
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?"
        },
        {
            "id": "problem_environment",
            "required": true,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What environment is the registry accessed from?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "AKS",
                    "text": "Azure Kubernetes Service"
                },
                {
                    "value": "ACI",
                    "text": "Azure Container Instance"
                },
                {
                    "value": "AzureAppService",
                    "text": "Azure App Service"
                },
                {
                    "value": "VM",
                    "text": "Azure Virtual Machine"
                },
                {
                    "value": "ACRTask",
                    "text": "ACR Task"
                },
                {
                    "value": "OtherAzure",
                    "text": "Another Azure Service"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ]
        },
        {
            "id": "problem_frequency",
            "required": true,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How are you accessing your registry?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "CLI",
                    "text": "Command Line"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ]
        },
        {
            "id": "problem_description",
            "required": true,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Exact portal actions or command line and expected results",
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---