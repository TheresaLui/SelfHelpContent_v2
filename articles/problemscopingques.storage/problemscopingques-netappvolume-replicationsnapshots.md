<properties
	articleId="problemscopingques-netappvolume-replicationsnapshot"
	pageTitle="Managing snapshots for replication volumes"
	description="Managing snapshots for replication volumes"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745370"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Managing snapshots for replication volumes
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "IManaging snapshots for replication volumes",
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
            "id": "policy_operation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you having issue managing your snapshot policy?",
            "watermarkText": "Which operation is failing",
			"dropdownOptions": [
				{
                    "value": "Create",
                    "text": "Create Policy"
                },
                {
                    "value": "Delete",
                    "text": "Delete Policy"
                },
				{
                    "value": "dont_know_answer",
                    "text": "None of the above"
                }
			],
            "required": true
        },  
		{
            "id": "netapp_account",
            "order": 3,
            "visibility": "operation == Delete",
            "controlType": "dropdown",
            "displayLabel": "NetApp Account",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.NetApp/netAppAccounts?api-version=2020-08-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
					"value": "dont_know_answer",
					"text": "None of the above"
                }
            },
            "dropdownOptions": [
                {
                    "value": "NoNetAppAccount",
                    "text": "Did not find the netapp account"
                }
            ],
            "required": false
        },
		{
            "id": "snapshot_policy",
            "order": 4,
            "visibility": "operation == Delete && netapp_account != null && netapp_account != dont_know_answer",
            "controlType": "dropdown",
            "displayLabel": "Select Snapshot Policy",
            "dynamicDropdownOptions": {
                "dependsOn": "netapp_account",
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.NetApp/netAppAccounts/{replaceWithParentValue}/snapshotpolicies?api-version=2020-08-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
					"value": "dont_know_answer",
					"text": "None of the above"
                },
                "textPropertyRegex": "[^/]+$",
                "valuePropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of snapshot policies.",
                    "text": "Unable to retrieve list of snapshot policies."
                }
            ],
            "required": false
        },
        {
            "id": "policy_enabled_assigned_volume",
            "order": 5,
            "visibility": "operation != Delete",
            "controlType": "dropdown",
            "displayLabel": "Is the snapshot policy assigned and enabled to volume?",
            "watermarkText": "",
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
                    "text": "None of the above"
                }
			],
            "required": false
        },
        {
            "id": "error_message",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message?",
            "watermarkText": "Copy the error message here",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
