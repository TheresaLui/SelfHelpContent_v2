<properties
	articleId="6d1aa869-d8c4-4457-9765-7b6f597cab59"
	pageTitle="Scoping Questions for Purview - data has privacy information but scanning did not find a classification"
	description="Scoping Questions for Purview - data has privacy information but scanning did not find a classification"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783248"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview My data has privacy information but scanning did not find a classification
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
