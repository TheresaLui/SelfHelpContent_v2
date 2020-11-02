<properties
	articleId="problemscopingques-netappvolume-backupoperator"
	pageTitle="Unable to add backup operator"
	description="Unable to add backup operator"
	authors="b-avaish"
	ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777926"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to add backup operator
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to add backup operator",
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
            "id": "ostypevm",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Is the username a valid username on the active directory?"
            "required": true
        },
		{
            "id": "nfspackages",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are NFS packages installed in VM?",
            "watermarkText": "Are NFS packages installed in VM?",
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