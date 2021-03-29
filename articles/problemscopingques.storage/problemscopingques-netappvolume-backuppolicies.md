<properties
	articleId="problemscopingques-netappvolume-backuppolicies"
	pageTitle="Unable to create or delete backup policy"
	description="Unable to create or delete backup policy"
	authors="b-avaish"
	ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32781858"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to create or delete backup policy
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to create or delete backup policy",
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
            "id": "operation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which operation is failing",
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
        "id": "issue_nature",
        "order": 3,
			"visibility": "operation == Delete",
        "controlType": "dropdown",
        "displayLabel": "Are you sure no volume is configured to the backup policy which you want to delete?",
        "watermarkText": "Are you sure no volume is configured to the backup policy which you want to delete?",
        "dropdownOptions": [{
            "value": "Yes",
            "text": "Yes"
        }, {
            "value": "No",
            "text": "No"
        }, {
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
    },
		{
            "id": "netapp_account",
            "order": 4,
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
            "required": true
        },
		{
            "id": "backup_policy_name",
            "order": 5,
            "visibility": "operation == Delete && netapp_account != null && netapp_account != dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Backup Policy name",
            "watermarkText": "Give the name of backup policy which is not getting deleted",
            "required": true
            },
        {
            "id": "problem_description",
            "order": 6,
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