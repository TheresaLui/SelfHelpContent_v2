<properties
	pageTitle="Storage File Share mounting issues - Windows"
	description="Storage File Share mounting issues - Windows"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602765"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="bf5acf40-b1c1-4cd9-b96d-023163fbf5db"
/>
# Storage File Share mounting issues - Windows
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage File Share mounting issues - Windows",
    "fileAttachmentHint": "",
    "diagnosticCard": {
		"title": "What caused my Azure Files mount issue on Windows?",
    	"description": "Our Azure Files mount troubleshooter can help you troubleshoot and solve your problem.",
    	"insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure that File Share or File Path provided is in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
	},
    "formElements": [
        {
            "id": "file_share_or_path",
            "order": 0,
            "controlType": "textbox",
            "displayLabel": "File Share or File path",
            "watermarkText": "'FileShare' or 'FileShare/FileName'",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "mount_location",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Location where File Share is being mounted",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "same_region",
                    "text": "Azure VM is in same region as the Azure File Share"
                },
                {
                    "value": "different_region",
                    "text": "Azure VM is in different region than the Azure File Share"
                },
                {
                    "value": "on_premises",
                    "text": "Client is outside Azure"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "os_version",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Windows version where File Share is being mounted",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "windows7",
                    "text": "Windows 7"
                },
                {
                    "value": "windows8",
                    "text": "Windows 8 or above"
                },
                {
                    "value": "server2008R2",
                    "text": "Windows Server 2008 R2"
                },
                {
                    "value": "server2012",
                    "text": "Windows Server 2012 or above"
                },
                {
                    "value": "old_windows",
                    "text": "Below Windows 7 or Windows Server 2008 R2"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "mount_error",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Windows mount error",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "error5",
                    "text": "System error 5 has occurred. Access is denied."
                },
                {
                    "value": "error53",
                    "text": "System error 53 has occurred. The network path was not found."
                },
                {
                    "value": "error64",
                    "text": "System error 64 has occurred. The specified network name is no longer available."
                },
                {
                    "value": "error67",
                    "text": "System error 67 has occurred. The network name cannot be found."
                },
                {
                    "value": "error86",
                    "text": "System error 86 has occurred. The specified network password is not correct."
                },
                {
                    "value": "error87",
                    "text": "System error 87 has occurred. The parameter is incorrect."
                },
                {
                    "value": "error1816",
                    "text": "System error 1816 has occurred. Not enough quota is available to process this command."
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "error_other",
            "order": 4,
            "visibility": "mount_error == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Error message",
            "watermarkText": "Error message received",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ]
}
---
