<properties
pageTitle="Missing Manifest or Tag"
description="Missing Manifest or Tag"
service="microsoft.containerregistry"
authors="nathana1"
ms.author="nathana"
selfHelpType="problemScopingQuestions"
supportTopicIds="32680714"
productPesIds="16213"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="problemscoping-missing-manifest"
schemaVersion="1"
	ownershipId="ContainerRegistry_Runtime"
/>
# Missing Manifest or Tag
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Missing Manifest or Tag",
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
            "controlType": "textbox",
            "displayLabel": "Name of missing manifest/tag",
            "watermarkText": "Name of missing manifest/tag"
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