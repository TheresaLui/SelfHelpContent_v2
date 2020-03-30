<properties
         pageTitle="Scoping questions for Azure portal"
         description="Scoping questions for Azure portal specific troubleshooting"
         authors="sansom,johirsch"
         ms.author="sansom"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32630411,32630412,32630435,32630456"
         productPesIds="13491"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="e31bdba2-c7ff-48c0-a2b3-d5bbd10ab7e4"
	ownershipId="AzureData_AzureSQLDB"
/>
# Questions for Azure Portal Issues
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
            "watermarkText": "Press 'Ctrl+Alt+D' and copy Session ID from bottom right popup",
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
                    "text": "Learn more - <a href='https://blogs.msdn.microsoft.com/benjaminperkins/2016/10/18/capture-a-trace-for-troubleshooting-azure-portal-issues/'>how to capture a browser network trace</a>"
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
