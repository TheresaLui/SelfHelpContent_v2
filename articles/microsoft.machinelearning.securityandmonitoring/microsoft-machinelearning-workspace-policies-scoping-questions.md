<properties
	pageTitle="Policies"
	description="Policies"
	infoBubbleText="Policies"
	service="microsoft.machinelearning.workspace"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32783452"
	productPesIds="16644"
    schemaVersion="1"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.workspace.policies.scoping.q"
	ownershipId="AzureML_AzureMachineLearningServices"
/>


# Policies
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Policies",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "policy_type",
            "order": 1,
            "controlType": "radiobuttongroup",
            "displayLabel": "Which kind of policies are you facing issues with?",
            "radioButtonOptions": [
                {
                    "value": "Built-in Policies",
                    "text": "Built-in Policies"
                },
                {
                    "value": "Custom Policies",
                    "text": "Custom Policies"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
