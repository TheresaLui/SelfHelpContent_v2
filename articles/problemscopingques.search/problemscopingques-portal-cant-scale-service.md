<properties
	pageTitle="Portal/I can’t scale the service in the portal"
	description="Issues scaling an Azure Cognitive Search service in the portal"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681347"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="833ef6d4-7df5-48fa-bccd-042aeff5be30"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issues scaling an Azure Cognitive Search service from the portal
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues scaling an Azure Cognitive Search service in the portal",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the issue you had scaling your service",
            "required": true,
            "useAsAdditionalDetails": true
        },
		{
            "id": "issue_choice",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What scale operation were you doing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "scaling_up",
                    "text": "Scaling Up"
                },
                {
                    "value": "scaling_down",
                    "text": "Scaling Down"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
		{
            "id": "scale_timeframe",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Has the scale operation been in a provisioning state for longer than 6 hours?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem last occur?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---