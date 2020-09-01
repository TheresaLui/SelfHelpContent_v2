<properties
	pageTitle="Move Services to Another Subscription"
	description="Move Services to Another Subscription"
	articleId="moveservicestoanothersubscription"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632956"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Move Services to Another Subscription
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Move Services to Another Subscription",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "sourcesubscriptionid_details",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "Select Source (FROM) Subscription ID",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions?api-version=2014-04-01",
                "jTokenPath": "value",
                "textProperty": "displayName,subscriptionId",
                "textTemplate": "{displayName} ({subscriptionId})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "dont_know_answer",
                    "text": "Not in the list"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "sourcesubscriptionid1_details",
            "order": 2,
            "visibility": "sourcesubscriptionid_details == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Provide the Source (FROM) Subscription ID",
            "required": false
        },
        {
            "id": "destinationsubscriptionid_details",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select Destination (TO) Subscription ID",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions?api-version=2014-04-01",
                "jTokenPath": "value",
                "textProperty": "displayName,subscriptionId",
                "textTemplate": "{displayName} ({subscriptionId})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "dont_know_answer",
                    "text": "Not in the list"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "destinationsubscriptionid1_details",
            "order": 4,
            "visibility": "destinationsubscriptionid_details == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Provide the Destination (TO) Subscription ID",
            "required": false
        },
        {
            "id": "services_details1",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Move all Services or selective Services?",
            "watermarkText": "Move all Services or selective Services ",
            "dropdownOptions": [
                {
                    "value": "All Services",
                    "text": "All Services"
                },
                {
                    "value": "Selective Services",
                    "text": "Selective Services"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "services_details2",
            "order": 6,
            "visibility": "services_details1 == Selective Services",
            "controlType": "multilinetextbox",
            "displayLabel": "Please list the services",
            "required": false
        },
        {
            "id": "requesterrole_details",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Requestor's current role assigned to the subscription",
            "watermarkText": "Select the Requestor's current role assigned to the subscription",
            "dropdownOptions": [
                {
                    "value": "ARM",
                    "text": "ARM"
                },
                {
                    "value": "ASM",
                    "text": "ASM"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Error message (if applicable)",
            "watermarkText": "Provide any error message or additional information about your issue",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
