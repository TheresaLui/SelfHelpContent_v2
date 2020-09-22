<properties
	pageTitle="problemscopingquestions machinelearning compute instance"
	description="Problem creating, managing or accessing compute instance - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="SturgeonMi"
	ms.author="vijetajo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745197,32745198,32690861"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingquestions-machinelearning-computeinstance"
	ownershipID="AzureML_AzureMachineLearningServices"
/>


# Problem creating, managing or accessing compute instance - scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem creating, managing or accessing compute instance - scoping questions",
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
			"id": "problem_computeinstancename",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What is the name of compute instance?",
			"required": true
	},
		{
			"id": "problem_storagevnet",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Is the workspace storage account attached to a virtual network?",
			"required": false
	},
		{
			"id": "problem_description",
			"order": 4,
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


