<properties
	articleId="problemscopingques-netappvolume-adconnector"
	pageTitle="Unable to create or update AD connector"
	description="Unable to create or update AD connector"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777926"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to create or update AD connector
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to create or update AD connector",
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
            "id": "netapp_account",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "NetApp Account",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.NetApp/netAppAccounts?api-version=2019-11-01",
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
            "id": "variable",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Issue with which feature?",
            "watermarkText": "Select the feature or variable that is causing the issue",
			"dropdownOptions": [
				{
                    "value": "BackupOperator",
                    "text": "Backup Operator"
                },
                {
                    "value": "AESencryption",
                    "text": "AES encryption"
                },
				{
                    "value": "LDAPsigning",
                    "text": "LDAP signing"
                },
				{
                    "value": "dont_know_answer",
                    "text": "None of the above"
                }
			],
            "required": false
        },
		{
            "id": "backupuser",
            "order": 4,
            "controlType": "dropdown",
			"visibility": "variable != null && variable == BackupOperator",
            "displayLabel": "Is the username a valid username on the Active Directory?",
            "watermarkText": "Is the username a valid username on the Active Directory?",
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
	   "id": "PTRrecord",
	   "order": 5,
	   "controlType": "dropdown",
	   "visibility": "variable != null && variable == LDAPsigning",
           "displayLabel": "Does a PTR record exist for the AD host machine in the reverse lookup zone ?",
	   "watermarkText": "Does a PTR record exist for the AD host machine in the reverse lookup zone ?",
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
