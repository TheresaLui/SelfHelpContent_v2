<properties
                pageTitle="Networking/Application Gateway"
                description="Networking/Application Gateway"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637179"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-application-gateway"
	ownershipId="Compute_AzureKubernetesService"
/>
# Application Gateway
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cluster failed state",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "getErrorMsg",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message did you receive while performing this operation, if any?",
            "required": false
        },
        {
            "id": "getBackendPoolDetails",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How’s you backend pool configured?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Through Load Balancer",
                    "text": "Through Load Balancer"
                },
                {
                    "value": "Through AKS nodes",
                    "text": "Through AKS nodes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I am not sure"
                }
            ],
            "required": false
        },
        {
            "id": "getAppGatewayVersion",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What version of the application gateway is being used?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Version 1",
                    "text": "Version 1"
                },
                {
                    "value": "Version 2",
                    "text": "Version 2"
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
