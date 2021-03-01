<properties
	articleId="problemscopingques-netappvolume-assignbackuppolicy"
	pageTitle="Issue while assigning backup policy to a volume"
	description="Issue while assigning backup policy to a volume"
	authors="b-avaish"
	ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32781856"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issue while assigning backup policy to a volume
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue while assigning backup policy to a volume",
    "fileAttachmentHint": "",
    "formElements": [
		{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
<<<<<<< HEAD
		{
            "id": "Policy_creation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are the snapshot policy and backup policy created successfully?",
            "watermarkText": "Are the snapshot policy and backup policy created successfully?",
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
            "required": true
        },
		{
            "id": "netapp_account",
            "order": 3,
=======
               {
            "id": "netapp_account",
            "order": 2,
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
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
<<<<<<< HEAD
		{
            "id": "backup_policy",
            "order": 4,
            "visibility": "netapp_account != null && netapp_account != dont_know_answer",
=======
                {
            "id": "backup_policy",
            "order": 3,
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
            "controlType": "dropdown",
            "displayLabel": "Select Backup Policy",
            "dynamicDropdownOptions": {
                "dependsOn": "netapp_account",
<<<<<<< HEAD
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.NetApp/netAppAccounts/{replaceWithParentValue}/backuppolicies?api-version=2020-09-01",
=======
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.NetApp/netAppAccounts/{replaceWithParentValue}/backuppolicies?api-version=2020-08-01",
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
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
                    "value": "Unable to retrieve list of backup policies.",
                    "text": "Unable to retrieve list of backup policies."
                }
            ],
            "required": false
        },
<<<<<<< HEAD
		{
=======
                {
            "id": "volume_name",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Select Volume",
            "dynamicDropdownOptions": {
                "dependsOn": "netapp_account",
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NetApp/netAppAccounts/{accountName}/capacityPools/{poolName}/volumes/{volumeName}?api-version=2020-08-01",
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
                    "value": "Unable to retrieve volumes.",
                    "text": "Unable to retrieve volumes."
                }
            ],
            "required": false
        },
        {
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
            "id": "problem_description",
            "order": 5,
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