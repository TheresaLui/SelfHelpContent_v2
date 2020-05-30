<properties pageTitle="SQL Server replication"
	 description="SQL Server replication"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633521"
	 productPesIds="14745"
	 cloudEnvironments="public,fairfax, usnat, ussec"
	 schemaVersion="1"
	 articleId="ed9f7860-2036-402d-8f05-9fed033a6e35"
	ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server replication
---
{
    "resourceRequired": false,
    "title": "SQL Server replication",
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
            "id": "whatKind",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What kind of SQL Server replication are you using?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Transactional",
                    "value": "Transactional"
                },
                {
                    "text": "Merge",
                    "value": "Merge"
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
