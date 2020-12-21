<properties
	pageTitle="Storage account upgrade to premium tier"
	description="Issue with storage account premium tier"
	authors="Lea Akkari"
    ms.author="leakkari"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32691092"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="A6BFE67E-FDC6-4976-9B75-90C8E272EC52"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Storage account premium tier
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Issue with storage account premium tier",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Want to troubleshoot an issue with premium tier?",
        "description": "Please fill in the information below to find a solution.",
        "insightNotAvailableText": "Our troubleshooter did not find any issue. Please ensure the information provided is accurate and in the approved format. Also, see our manual steps below to find a solution."
    },
    "formElements": [
        {
            "id": "failure_scenario",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which scenario did you have issue with",
            "dropdownOptions": [
                {
                    "value": "move_account_to_new_subId",
                    "text": "Cannot create premium StorageV2 (general purpose v2) account with geo replication type (GRS/RA-GRS/GZRS/RA-GZRS)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "diagnosticInputRequiredClients": "ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true,
            "diagnosticInputRequiredClients": "ASC"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
