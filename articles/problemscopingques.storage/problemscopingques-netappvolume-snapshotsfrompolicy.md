<properties
	articleId="problemscopingques-netappvolume-snapshotsfrompolicy"
	pageTitle="Issues with snapshot creation from policy"
	description="Issues with snapshot creation from policy"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777919"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issues with snapshot creation from policy
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues with snapshot creation from policy",
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
        "displayLabel": "Is the snapshot policy enabled and assigned to volume?",
        "watermarkText": "Choose whether policy is enabled and assigned to volume",
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
            "id": "policy_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Policy Name",
            "watermarkText": "Policy Name",
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
