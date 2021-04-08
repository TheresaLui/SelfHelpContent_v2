<properties
	articleId="a6a2d935-7321-4ae7-9b31-ee82c7ae8777"
	pageTitle="Scoping Questions for Purview Provisioning Cannot Delete Account"
	description="Scoping Questions for Purview Provisioning Cannot Delete Account"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783212"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview Cannot Delete Account
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview Cannot Delete Account",
    "fileAttachmentHint": "If using SDKs to deploy, please attach the deployment",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
         {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Brief description of the issue",
            "watermarkText": "Please provide any information related to this issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
       {
            "id": "error_msg",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Complete error message (if any)",
            "watermarkText": "Please provide error message you are getting",
            "required": false
        },
       {
            "id": "frequency",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Is this issue intermittent or consistent?",
            "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
                },
                {
                    "value": "Consistent",
                    "text": "Consistent"
                },
		{
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
