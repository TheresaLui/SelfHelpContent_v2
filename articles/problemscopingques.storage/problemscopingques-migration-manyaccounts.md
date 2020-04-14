<properties
	pageTitle="Migrate to ZRS, GZRS, RA-GZRS"
	description="Migrate to ZRS, GZRS, RA-GZRS"
	authors="Passaree"
        ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32605567,32691090"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="ED05B7F3-35E8-4F28-B3A3-FBFF20E2B301"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Migrate to ZRS, GZRS, RA-GZRS
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "How to choose data migration solution",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Want to check Replication Eligibility?",
        "description": "Check replication eligibility before proceed",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with the replication. Please ensure the information provided is accurate and in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
         {
            "id": "target_replication_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Target replication type",
 	        "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "zrs",
                    "text": "To ZRS"
                },
		        {
                    "value": "gzrs",
                    "text": "To GZRS"
                },
		        {
                    "value": "ragzrs",
                    "text": "To RA-GZRS"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
	{
            "id": "storage_account_from",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Storage accounts from",
            "watermarkText": "AccountName1;AccountName2;AccountName3",
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
