<properties
                pageTitle="Networking/Ingress-Egress related"
                description="Networking/Ingress-Egress related"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637197"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-ingress-egress"
	ownershipId="Compute_AzureKubernetesService"
/>
# Ingress-Egress related
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Ingress Egress related issue",
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
            "id": "getIngressOrEgress",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have problem with Ingress or Egress?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Ingress",
                    "text": "Ingress"
                },
                {
                    "value": "Egress",
                    "text": "Egress"
                }
            ],
            "required": false
        },
        {
            "id": "getErrorMsg",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message did you receive while performing this operation, if any?",
            "required": false
        },
        {
            "id": "getRouteTableOrNSG",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you using custom Route Table or NSG in your VNET configuration?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Route Table",
                    "text": "Route Table"
                },
                {
                    "value": "NSG",
                    "text": "NSG"
                },
                {
                    "value": "Both",
                    "text": "Both"
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
            "order": 5,
            "controlType": "multilinetextbox",
            "watermarkText": "Please provide your ingress configuration",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
