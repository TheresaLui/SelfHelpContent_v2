<properties
	articleId="c80f11fd-e2d0-463c-a55a-12edd3b46d94"
	pageTitle="Scoping Questions for Purview Provisioning Cannot Create Account"
	description="Scoping Questions for Purview Provisioning Cannot Create Account"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783211"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview Cannot Create Account
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview Cannot Create Account",
    "fileAttachmentHint": "If using SDKs to deploy, please attach the deployment script.",
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
        },
        {
            "id": "correlation_id",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "Please provide the correlation id (if any)",
            "required": false
        },
        {
            "id": "name_region",
            "order": 50,
            "controlType": "textbox",
            "displayLabel": "What is the name and Region of the account you tried to create?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
