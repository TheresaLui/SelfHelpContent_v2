<properties
	pageTitle="Blob Object Replication Issues"
	description="Blob Object Replication Issues"
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
# Blob Object Replication Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Blob Object Replication Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "source_container",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Source container name",
            "required": true
        },
        {
            "id": "destination_account",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Destination account name",
            "required": true
        },
        {
            "id": "destination_container",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Destination container name",
            "required": true
        },
        {
            "id": "issue_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Issue Type,
            "watermarkText": "Select the issues you are facing",
            "dropdownOptions": [
              {
                "value": "slow_replication_poor_replication_performance",
                "text": "Slow replication/Poor replication performance"
              },
              {
                "value": "missing_data_on_destination_container",
                "text": "Missing data on destination container"
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
