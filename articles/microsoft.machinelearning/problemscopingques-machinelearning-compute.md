<properties
	pageTitle="problemscopingquestions machinelearning compute"
	description="Compute cluster in a bad state - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="SturgeonMi"
	ms.author="brendalee"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690842,32690843, 32780560"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingquestions-machinelearning-compute"
	ownershipID="AzureML_AzureMachineLearningServices"
/>


# Compute cluster in a bad state - scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Compute cluster in a bad state - scoping questions",
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
			"id": "problem_vnetnsgrules",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "In case of creation in a virtual network, can you provide the NSG rules you have?",
			"required": false
	},
  {
			"id": "problem_SDKver",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What version of SDK are you using??",
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

