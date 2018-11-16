<properties
	pageTitle="Scoping questions for Cloud Services Deployment Failures"
	description="Scoping questions for Cloud Services Deployment Failures"
	authors="ChiragPavecha"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32565474, 32565476, 32565478, 32565479, 32591243, 32565480"
	productPesIds="13185"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="0c92c988-7e99-41de-b03a-ad3ecd4074d6"
/>
# Cloud Services Deployment Failures
---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Issue description"
                },
                {
                    "text": "Time of Deployment Failure with timezone"
                },
                {
                    "text": "Error Message for failed Deployment"
                },
                {
                    "text": "OperationId, if available"
                }
            ]
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ]
}
---