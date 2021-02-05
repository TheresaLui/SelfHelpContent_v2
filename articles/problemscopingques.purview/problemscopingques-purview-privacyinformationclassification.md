<properties
	articleId="9ebd4088-fa60-4665-b27f-2beafb83aede"
	pageTitle="Scoping Questions for Purview Wrong or Missing Classification"
	description="Scoping Questions for Purview Wrong or Missing Classification"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783271"
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
    "fileAttachmentHint": "In case it’s a custom classification, please add screenshot of the configured classification",
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
            "id": "classification_type",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "Is it a System Classification or Custom Classification? ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "System Classification",
                    "text": "System Classification"
                },
                {
                    "value": "Custom Classification",
                    "text": "Custom Classification"
                },
		            {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
              ],
            "required": true
        },
      
        {
            "id": "expected_classification",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "Which classifications  were expected?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
