<properties
                pageTitle="Networking/Load balancer"
                description="Networking/Load balancer"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637198"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-load-balancer"
	ownershipId="Compute_AzureKubernetesService"
/>
# Load balancer
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
            "id": "getInboundOutbound",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this issue related to Inbound or Outbound traffic?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Inbound Traffic",
                    "text": "Inbound Traffic"
                },
                {
                    "value": "Outbound Traffic",
                    "text": "Outbound Traffic"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I am not sure"
                }
            ],
            "required": false
        },
        {
            "id": "getInboundDetails",
            "order": 4,
            "visibility": "getInboundOutbound == Inbound Traffic",
            "controlType": "dropdown",
            "displayLabel": "Can the AKS node be accessed via the port(s) specified in the load balancer probe(s)?",
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
                    "text": "I don't know"
                }
            ],
            "required": false
        },
        {
            "id": "getOutboundDetails",
            "order": 5,
            "visibility": "getInboundOutbound == Outbound Traffic",
            "controlType": "dropdown",
            "displayLabel": "Are there many connections being established in a short time?",
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
                    "text": "I don't know"
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
