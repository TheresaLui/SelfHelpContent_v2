<properties
                pageTitle="Networking/API Server Connectivity and Timeout"
                description="Networking/API Server Connectivity and Timeout"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32683757"
                productPesIds="16450"
                cloudEnvironments="Public,Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-api-server-timeout"
	ownershipId="Compute_AzureKubernetesService"
/>
# API Server Connectivity and Timeout
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "API Server Connectivity",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the last time you experienced this issue?",
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
            "id": "getPublicIPTimeOutChanged",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you tried to adjust the timeout value for PublicIP?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "infoBalloonText": "You can adjust the default <a href='https://docs.microsoft.com/azure/aks/load-balancer-standard#configure-outbound-ports-and-idle-timeout'>timeout value of Public IP</a> which is 4mins for Basic LB",
            "required": false
        },
        {
            "id": "getPortSettings",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you configured the required port for AKS cluster?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "infoBalloonText": "Check the list of <a href='https://docs.microsoft.com/azure/aks/limit-egress-traffic#required-ports-and-addresses-for-aks-clusters'>required ports</a> for AKS cluster.",
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
