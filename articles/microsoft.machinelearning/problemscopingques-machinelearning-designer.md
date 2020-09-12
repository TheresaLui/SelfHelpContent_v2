<properties
	pageTitle="problemscopingques problem creating or managing designer pipeline"
	description="Problem creating or managing designer pipeline - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="SturgeonMi"
	ms.author="keli19"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690869,32690867,32690892,32690871"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingques-machinelearning-designer"
	ownershipID="AzureML_AzureMachineLearningServices"
/>

# Problem creating or managing designer pipeline: scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem creating or managing designer pipeline",
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
			"id": "problem_requestid",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "RequestId in the error message",
			"required": false
	},
		{
			"id": "problem_pipelinerunid",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Pipeline run/pipeline draft URL",
			"required": false
	},
		{
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide detailed information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description"
				}, {
					"text": "Step Run ID (Find under *Details** tab in the module right pane)"
				}, {
					"text": "Detailed error message"
				}
			]
		}
	]
}
---

