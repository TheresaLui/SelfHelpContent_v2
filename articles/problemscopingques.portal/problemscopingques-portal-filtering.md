<properties
         pageTitle="Scoping questions for Azure portal subscription or directory filtering issue"
         description="Scoping questions for Azure portal subscription or directory filtering specific troubleshooting"
         authors="sansom"
         ms.author="sansom"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32628244"
         productPesIds="15739"
         cloudEnvironments="public, Fairfax, usnat, ussec, blackforest, mooncake"
         schemaVersion="1"
         articleId="problemscopingquesportalfiltering"
	ownershipId="Compute_AzurePortal"
/>
# Questions for Azure Portal subscription or directory filtering issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Scoping questions for Azure portal subscription or directory filtering issue",
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
            "displayLabel": "Browser network trace or any other error message (if applicable)",
            "watermarkText": "Provide the browser network trace or any error message or additional information about your issue",
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
                    "text": "Provide details of the subscription or directory filtering issue you are experiencing"
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
