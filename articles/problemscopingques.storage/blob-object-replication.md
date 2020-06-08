<properties
	pageTitle="Blob object replication"
	description="Blob object replication issues"
	authors="Sijia"
    ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740858"
	productPesIds="16459"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="dd1bd8fe-1876-49a5-90b3-134ac70e75d9"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Blob object replication issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Blob object replication issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "source_container",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Source container name",
            "required": true
        },
        {
            "id": "destination_account",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Destination account name",
            "required": false
        },
        {
            "id": "destination_container",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Destination container name",
            "required": false
        },
        {
            "id": "issue_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Issue Type",
            "watermarkText": "Select the issues you are facing",
            "dropdownOptions": [
              {
                "value": "slow_replication_poor_replication_performance",
                "text": "Slow replication/Poor replication performance"
              },
              {
                "value": "missing_data_on_destination_container",
                "text": "Missing data on destination container"
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
