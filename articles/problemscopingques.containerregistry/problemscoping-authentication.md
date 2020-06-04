<properties
pageTitle="Authentication Issues"
description="Authentication Issues"
service="microsoft.containerregistry"
authors="nathana1"
ms.author="nathana"
selfHelpType="problemScopingQuestions"
supportTopicIds="32680715,32680716,32680717"
productPesIds="16213"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="problemscoping-authentication"
schemaVersion="1"
	ownershipId="ContainerRegistry_Runtime"
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
            "id": "problem_auth_method",
            "required": true,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What authentication method was used?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Admin",
                    "text": "Admin User"
                },
                {
                    "value": "Individual",
                    "text": "Individual AAD Account"
                },
                {
                    "value": "Service",
                    "text": "Service Principal"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue (such as the output from 'az acr check-health --name myregistry --ignore-errors --yes')",
            "required": true,
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