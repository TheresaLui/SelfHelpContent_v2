<properties pageTitle="Automated Patching"
	 description="Automated Patching"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633492"
	 productPesIds="14745"
	 cloudEnvironments="public,fairfax"
	 schemaVersion="1"
	 articleId="160f0c4b-5c22-492a-9e21-f7599696ed14"
	ownershipId="AzureData_AzureSQLVM"
/>
# Automated Patching
---
{
    "resourceRequired": false,
    "title": "Automated Patching",
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
            "id": "kind_of_patching",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which kind of patching do you need assistance with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Security Patches",
                    "value": "SecurityPatches"
                },
                {
                    "text": "SQL Server cumulative updates/Service Packs",
                    "value": "SQLCumulativeUpdatesAndServicePacks"
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
