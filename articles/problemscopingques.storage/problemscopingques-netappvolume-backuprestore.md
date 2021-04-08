<properties
	articleId="problemscopingques-netappvolume-backuprestore"
	pageTitle="Unable to restore volume from backup"
	description="Unable to restore volume from backup"
	authors="b-avaish"
	ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32781859"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to restore volume from backup
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to restore volume from backup",
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
            "id": "volume",
            "order": 2,
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
            "id": "backup_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Backup name",
            "watermarkText": "Give the name of Backup from which volume is not getting restored",
            "required": true,
            "useAsAdditionalDetails": true
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
