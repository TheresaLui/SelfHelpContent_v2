<properties
pageTitle="Performance Issues"
description="Performance Issues"
service="microsoft.containerregistry"
authors="nathana1"
ms.author="nathana"
selfHelpType="problemScopingQuestions"
supportTopicIds="32680727,32680729,32680723,32680728,32680730"
productPesIds="16213"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="problemscoping-performance"
schemaVersion="1"
	ownershipId="ContainerRegistry_Runtime"
/>
# Performance Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Performance Issues",
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
            "displayLabel": "How often does this occur?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Always",
                    "text": "Always"
                },
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not noticing any trend."
                }
            ]
        },
        {
            "id": "problem_description",
            "required": true,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue (such as the output from 'az acr check-health --name myregistry --ignore-errors --yes')",
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