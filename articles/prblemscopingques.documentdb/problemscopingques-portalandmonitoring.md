<properties
	pageTitle="CosmosDB Portal and Monitoring Issue"
	description="CosmosDB Portal and Monitoring Issue"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636780,32636799,32636767,32636790,32636811"
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
