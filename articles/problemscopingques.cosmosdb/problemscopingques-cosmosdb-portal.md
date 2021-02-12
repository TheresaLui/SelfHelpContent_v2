<properties
	pageTitle="CosmosDB Portal Issue"
	description="CosmosDB Portal Issue"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32688846"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="9a15edbc-1a5a-4e4d-8bd9-1d9e24f56c91"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Portal Issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB Portal Issues",
    "fileAttachmentHint": "Please attach a HAR file to expedite the investigation. Use [F12] to open the developer tools in your browser. Navigate to the Network tab. Reproduce the issue, while the network requests are being recorded. Save the network traces as a HAR file: in Chrome or Firefox, right-click inside the network pane of requests and select 'Save all as HAR'; in Edge or Internet Explorer, select the 'Export as HAR' command or type [Ctrl] + [S] in the Network tab.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
		{
            "id": "session_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide a Session Id for when you observe the issue.",
			"infoBalloonText": "Once the Portal has loaded and you've reproduced the issue, use [Ctrl] + [Alt] + [A] in your browser. This generates a PortalDiagnostics.json file that contains the Session Id as 'sessionId.'",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you were facing",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---