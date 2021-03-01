<properties
	articleId="problemscopingques-netappvolume-adhocbackup"
	pageTitle="Unable to create adhoc backup for a volume"
	description="Unable to create adhoc backup for a volume"
	authors="b-avaish"
	ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32781857"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to create adhoc backup for a volume
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to create adhoc backup for a volume",
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
        "id": "issue_nature",
        "order": 2,
        "controlType": "dropdown",
        "displayLabel": "Is backup configuration enabled for volume?",
        "watermarkText": "Is backup configuration enabled for volume?",
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
            "id": "volume_name",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Volume",
            "watermarkText": "Choose an option",
			"dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NetApp/netAppAccounts/{accountName}/capacityPools/{poolName}/volumes/{volumeName}?api-version=2020-09-01",
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
                    "value": "VolumeNotFound",
                    "text": "Did not find the volume"
                }
            ],
            "required": true
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