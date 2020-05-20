<properties
	pageTitle="Storage account replication type"
	description="Issue with changing storage account replication type"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32691089"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="90634BE9-6A50-44C1-85EF-DF95F5C14CA4"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Issue with changing storage account replication type
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue with changing storage account replication type",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Why do I have issue changing replication type for this storage account?",
        "description": "Our replication type troubleshooter can help you identify and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your storage account. Please ensure the selected storage account in the previous blade is the on you are having issue changing replication type."
    },
    "formElements": [
        {
            "id": "new_replication",
            "order": 0,
            "controlType": "dropdown",
            "displayLabel": "New replication type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "lrs",
                    "text": "LRS"
                },
                {
                    "value": "grs",
                    "text": "GRS"
                },
                {
                    "value": "ra_grs",
                    "text": "RA-GRS"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message received",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
