<properties
	pageTitle="CosmosDB Portal and Monitoring Issue"
	description="CosmosDB Portal and Monitoring Issue"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636780, 32636799, 32636767, 32636790, 32636811"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="2afe17a9-592e-4088-9842-ccef4f79151d"
/>
# CosmosDB Portal and Monitoring Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB Portal and Monitoring Issue",
    "fileAttachmentHint": "Please attach a HAR trace file. 
			Open the developer tools in Chrome or Edge, then reproduce your issue. After reproducing the issue, save the network traces as a HAR file
			-	In Chrome, right-click anywhere inside the Network pane and select 'Save as HAR with Content' or from the drop-down actions menu. 
			-	In Edge or Internet Explorer Click command to “Export as HAR” or typing [Ctrl] + [S]
			This will open a dialog allowing you to select where to save your HAR file. Please attach this HAR file to expedite the investigation of the Portal issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
		{
            "id": "problem_duration",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "How long was the issue observed?",
            "required": false
        },
		{
            "id": "session_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide the session Id for issue",
			"infoBalloonText": "Once the Portal has loaded, use [Ctrl] + [Alt] + [A] which will provide information about what subscriptions are currently loaded"
            "required": false
        },
		{
            "id": "database_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": false
        },
		{
            "id": "collection_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Collection name",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you were facing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
