<properties
	articleId="3219aca2-2d18-46c5-be16-39003aa173f6"
	pageTitle="Scoping Questions for Purview - I do not see any changes in my catalog"
	description="Scoping Questions for Purview - I do not see any changes in my catalog"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783234"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview - I do not see any changes in my catalog
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview - I do not see any changes in my catalog",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
         {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Brief description of the issue",
            "watermarkText": "Please provide any information related to this issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "policy_change",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "What changes are made to the policy?",
            "required": false
        },
        {
            "id": "change_time",
            "order": 50,
            "controlType": "textbox",
            "displayLabel": "When was the change made?",
            "required": false
        },
         {
            "id": "instance_name",
            "order": 60,
            "controlType": "textbox",
            "displayLabel": "What is the name of the Purview Instance?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
