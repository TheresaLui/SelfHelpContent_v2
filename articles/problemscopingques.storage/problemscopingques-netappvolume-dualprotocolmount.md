<properties
	articleId="problemscopingques-netappvolume-mountdualprotocol"
	pageTitle="Unable to mount dual protocol volume"
	description="Unable to mount dual protocol volume"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777925"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to mount dual protocol volume
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to mount dual protocol volume",
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
            "displayLabel": "What is the VM OS type where mount is done?",
            "watermarkText": "OS of VM where the volume is being mouted",
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
