<properties
	articleId="problemscopingques-netappvolume-assignsnapshotpolicy"
	pageTitle="Unable to assign snapshot policy to a volume"
	description="Unable to assign snapshot policy to a volume"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777920"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to assign snapshot policy to a volume
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to assign snapshot policy to a volume",
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
            "required": false
        },
		{
            "id": "snapshot_policy",
            "order": 3,
            "visibility": "netapp_account != null && netapp_account != dont_know_answer",
            "controlType": "dropdown",
            "displayLabel": "Select Snapshot Policy",
            "dynamicDropdownOptions": {
                "dependsOn": "netapp_account",
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.NetApp/netAppAccounts/{replaceWithParentValue}/snapshotpolicies?api-version=2019-11-01",
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
            "id": "problem_description",
            "order": 4,
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
