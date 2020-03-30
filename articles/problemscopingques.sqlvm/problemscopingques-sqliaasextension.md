<properties pageTitle="SQL Iaas Extension"
	 description="SQL Iaas Extension"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633515"
	 productPesIds="14745"
	 cloudEnvironments="public,fairfax"
	 schemaVersion="1"
	 articleId="27f7c53b-0bb5-4760-bcbf-7fd6d9122066"
	ownershipId="AzureData_AzureSQLVM"
/>
# SQL Iaas Extension
---
{
    "resourceRequired": false,
    "title": "SQL Iaas Extension",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "which_operation",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What operation do you need assistance with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Install the extension",
                    "value": "Install"
                },
                {
                    "text": "Remove the extension",
                    "value": "Remove"
                },
                {
                    "text": "Issues/errors using the extension",
                    "value": "Issues"
                },
                {
                    "text": "I’m not sure/don’t know",
                    "value": "dont_know_answer"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
