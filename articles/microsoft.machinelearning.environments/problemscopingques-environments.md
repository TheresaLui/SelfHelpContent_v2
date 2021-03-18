<properties
	pageTitle="Environment scoping questions"
	description="Environment scoping questions"
	ms.author="sagopal"
	supportTopicIds="32755203, 32690887, 32755204, 32755205, 32755206"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.environments.problemscopingques-environments.md"
  selfHelpType="problemScopingQuestions"
  ownershipId="AzureML_AzureMachineLearningServices"
  schemaVersion="1"
/>


# Environment build fails
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Environment build fails",
    "fileAttachmentHint": "Attach service logs and/or image build logs",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
	{
            "id": "package",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Are you experiencing package installation or update issues?",
            "required": false
        },
	{
            "id": "service_side",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Are you experiencing container registry or storage issues?",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
