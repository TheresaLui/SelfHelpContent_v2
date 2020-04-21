<properties
                pageTitle="Networking/DNS related"
                description="Networking/DNS related"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637188"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-dns-related"
	ownershipId="Compute_AzureKubernetesService"
/>
# DNS related
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
            "id": "getDNSIssueFromAKSNodes",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Does the DNS issue also occur from the AKS node itself?",
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
            "id": "getVnetNic",
            "order": 4,
            "visibility": "getDNSIssueFromAKSNodes == Yes",
            "controlType": "dropdown",
            "displayLabel": "Are you using custom DNS in the VNET/NIC?",
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
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "getConfigmap",
            "order": 5,
            "visibility": "getDNSIssueFromAKSNodes == No",
            "controlType": "dropdown",
            "displayLabel": "Are you using DNS configmap to specify DNS settings for the pods?",
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
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
