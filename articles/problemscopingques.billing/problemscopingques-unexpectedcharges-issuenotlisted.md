<properties
	pageTitle="Unexpected Charges-issuenotlisted"
	description="Unexpected Charges-issuenotlisted"
	articleId="unexpectedcharges-problemscopingquestions-issuenotlisted"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680683"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
# Unexpected Charges-issuenotlisted
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Unexpected Charges-issuenotlisted",
    "fileAttachmentHint": "Please attach the screenshot of the error (if any)",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Brief summary of the issue",
            "watermarkText": "Provide brief summary of the issue",
            "required": true
        },
	{
            "id": "error_details",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": false,
            "displayLabel": "Error message (if any)",
            "watermarkText": "",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
