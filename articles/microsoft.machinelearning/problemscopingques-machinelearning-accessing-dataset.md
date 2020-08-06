<properties
	pageTitle="problemscopingques-machinelearning-accessing-dataset"
	description="Problem accessing dataset or connecting to datastore - scoping questions"
	authors="SturgeonMi"
	ms.author="xunwan"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690860,32690849,32690851"
	productPesIds="16644"
	articleId="problemscopingques-machinelearning-accessing-dataset"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipID="AzureML_AzureMachineLearningServices"
	schemaVersion="1"
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
            		"required": true
        },
		{
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Version",
			"watermarkText": "Version details",
			"required": true
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Version details"
				}, {
					"text": "What version of azureml SDK are you using? What version azureml-dataprep SDK is installed?"
				}
			]
		}
	]
}
---

