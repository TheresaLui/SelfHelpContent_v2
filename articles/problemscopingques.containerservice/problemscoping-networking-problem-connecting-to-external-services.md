<properties
                pageTitle="Networking/Problems connecting to external services"
                description="Networking/Problems connecting to external services"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32683764"
                productPesIds="16450"
                cloudEnvironments="Public,Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-problem-connecting-to-external-services"
	ownershipId="Compute_AzureKubernetesService"
/>
# Problems connecting to external services
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problems connecting to external services",
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
            "id": "getPublicIPCapacity",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you validate that you have enough outbound IP capacity?",
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
            "infoBalloonText": "You must have enough <a href='https://docs.microsoft.com/azure/aks/load-balancer-standard#required-quota-for-customizing-allocatedoutboundports'>outbound IP capacity</a> based on the number of your node VMs and desired allocated outbound ports.",
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
