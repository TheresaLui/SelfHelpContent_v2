<properties
	pageTitle="problemscopingques machinelearning automl"
	description="Problem setting up or running automl experiments - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="Aniththa"
	ms.author="anumamah"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690882,32690835,32755240,32755241,32690866,32690853,32755242,32690880"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingques-problems related to automl"
	ownershipID="AzureML_AzureMachineLearningServices"
/>


# Problem creating or running automl experiments: scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem with AutoML experiments",
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
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Version",
			"watermarkText": "Version details",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Version details"
				}, {
					"text": "What version of azureml SDK are you using?"
				}
			]
		}
	]
}
---
