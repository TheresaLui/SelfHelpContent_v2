<properties
	pageTitle="Private Endpoint and Private DNS allowance request"
	description="Private Endpoint and Private DNS allowance request"
	infoBubbleText="Private Endpoint and Private DNS allowance request"
	service="microsoft.machinelearning.workspace"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32755238"
	productPesIds="16644"
    schemaVersion="1"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="059c5496-b775-4091-a4f6-61c983559cb9"
	ownershipId="AzureML_AzureMachineLearningServices"
/>


# Private Endpoint and Private DNS allowance request
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Private Endpoint and Private DNS allowance request",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "region",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What region(s) so you want to increase your quota in?",
            "required": false
        },
        {
            "id": "cmk_ws",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Are you using workspaces with customer-managed keys? If so, how many workspaces do you have?",
            "required": false
        },
        {
            "id": "acr",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Are your workspace container registries behind a virtual network? If so, how many container registries do you have?",
            "required": false
        },
        {
            "id": "aks",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Will you be using Azure Kubenernetes clusters that have private endpoints? If so, how many clusters will you have?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
