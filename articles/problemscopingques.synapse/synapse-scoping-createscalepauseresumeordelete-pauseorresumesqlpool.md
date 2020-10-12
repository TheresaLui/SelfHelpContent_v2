<properties
	schemaVersion = "1"
	selfHelpType = "problemScopingQuestions"
	cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	productPesIds = "15818"
	supportTopicIds = "32738785"
	pageTitle = "Create, Scale, Pause, Resume or Delete/Pause or Resume SQL pool"
	description = "Create, Scale, Pause, Resume or Delete/Pause or Resume SQL pool"
	articleId = "synapse-scoping-createscalepauseresumeordelete-pauseorresumesqlpool"
	authors = "saltug"
	ms.author = "saltug"
/>

# Create, Scale, Pause, Resume or Delete/Pause or Resume SQL pool

---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "title": "Pause or Resume SQL pool",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "required": true,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "infoBalloonText": ""
        },
        {
            "id": "dw_2",
            "order": 2,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "How long has this operation have been running?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "dw_3",
            "order": 3,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "If an error was displayed, what was the error message?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "problem_description",
            "order": 4,
            "required": true,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "infoBalloonText": "",
            "useAsAdditionalDetails": true
        }
    ]
}
---

