<properties
	articleId="problemscopingques-sqlmi-portalandtools-portal"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture Azure Portal related issues"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637240"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Scoping questions for Azure portal",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "session_id_value",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Session ID",
            "watermarkText": "Press 'Ctrl+Alt+D' and copy Session ID from bottom right dialog box",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Learn more - <a href='https://docs.microsoft.com/azure/azure-portal/capture-browser-trace'>how to capture a browser network trace</a>"
                },
                {
                    "text": "Issue description."
                },
                {
                    "text": "Name of the resource or resource type in the subscription that you are seeing issue with"
                }
            ]
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "Cleared browser cache",
                    "text": "Cleared browser cache"
                },
                {
                    "value": "Firewall settings on the machine/proxy are configured to allow the required URLs",
                    "text": "Firewall settings on the machine/proxy are configured to allow the required URLs"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "Logging into the right directory",
                    "text": "Logging into the right directory"
                },
                {
                    "value": "Changed directory to verify portal again",
                    "text": "Changed directory to verify portal again"
                },
                {
                    "value": "Verified browser version is supported",
                    "text": "Verified browser version is supported"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
