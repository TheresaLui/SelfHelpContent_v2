<properties
	pageTitle="problemscopingquestions machinelearning compute"
	description="Attach compute - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="SturgeonMi"
	ms.author="brendalee"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690886, 32746413"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingquestions-machinelearning-attachcompute"
	ownershipID="AzureML_AzureMachineLearningServices"
/>


# Attach compute - scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Attach compute - scoping questions",
    "fileAttachmentHint": "",
    "formElements":
    [
		{
            		"id": "problem_start_time",
            		"order": 1,
            		"controlType": "datetimepicker",
            		"displayLabel": "When did the problem start?",
            		"required": false
        },
		{
			"id": "problem_computename",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What is the name of the compute resource?",
			"required": true
	},
		{
			"id": "problem_networking",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What networking configurations / firewalls do you have applied?",
			"required": false
	},
  {
			"id": "problem_errormessagedetails",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the error message and correlation ID?",
			"required": false
	},
		{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Issue description."
				}
			]
		}
	]
}
---
