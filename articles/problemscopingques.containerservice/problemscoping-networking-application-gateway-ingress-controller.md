<properties
                pageTitle="Networking/Application Gateway Ingress Controller"
                description="Networking/Application Gateway Ingress Controller"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32689809"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-application-gateway-ingress-controller"
	ownershipId="Compute_AzureKubernetesService"
/>
# Application Gateway
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Application Gateway Ingress Controller",
    "fileAttachmentHint": "Please upload your YAML configuration file",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "getAdvanceNetworkingEnabled",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have advance networking enabled?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I am not sure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
