<properties
	articleId="problemscopingques-netappvolume-SMBADIssue"
	pageTitle="Issues with SMB Volumes,DNS,Active Directory"
	description="Issues with SMB Volumes,DNS,Active Directory"
	authors="b-avaish"
    ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740758"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to Create Continuously Available SMB Share
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues with SMB Volumes,DNS,Active Directory",
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
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message received",
            "required": false
        },
        {
            "id": "SMBADIssue",
            "order": 3,
            "ControlType": "dropdown",
            "displayLabel": "Is the username provided in the security privilege block the same as the domain username used for installing Microsoft SQL server?",
            "watermarkText": "Is the username given in security privilege block same as domain username used for installing Microsoft SQL server?",
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
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
