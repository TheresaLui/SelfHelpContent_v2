<properties
	articleId="problemscopingques-queryfailures-general"
	pageTitle="problemscopingques-queryfailures-general"
	description="Scoping questions to capture start time for query failures"
	authors="radennis"
	ms.author="prvavill"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32613464,32613482,32613506"
	productPesIds="16602"
	cloudEnvironments="Public"
	schemaVersion="1"
	ownershipId="AzureDataExplorer_Kusto"
/>
# Azure Data Explorer Query Failures
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Data Explorer query failures troubleshooter",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "ProblemStartTime",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "RootActivityId",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Do you have RootactivityId of the affected query?",
            "watermarkText": "",
            "required": false
        }
    ]
}
---