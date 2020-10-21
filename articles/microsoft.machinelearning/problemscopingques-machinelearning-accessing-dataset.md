<properties
	pageTitle="problemscopingques machinelearning accessing dataset"
	description="Problem accessing dataset or connecting to datastore - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="SturgeonMi"
	ms.author="xunwan"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690860,32690849,32690851"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="b2dad4ce-43d2-4ed1-bac1-e9744d7a32fa"
	ownershipID="AzureML_AzureMachineLearningServices"
/>


# Problem accessing dataset or connecting to datastore: scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem accessing dataset or connecting to datastore",
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
			"id": "problem_runid",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What is the related RunId?",
			"required": false
	},
		{
			"id": "problem_datasetid",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What is the related DatasetId?",
			"required": false
	},
			{
			"id": "problem_version",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What version of azureml SDK are you using?",
			"required": false
	},
		{
			"id": "problem_description",
			"order":5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Describe what is the problem you are facing",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Details"
				}, {
					"text": "Describe what is the problem you are facing. What version of azureml-dataprep SDK is installed? What is your VNET setting if your storge is behind VNET? (More details can help us understand the problem better)"
				}
			]
		}
	]
}
---

