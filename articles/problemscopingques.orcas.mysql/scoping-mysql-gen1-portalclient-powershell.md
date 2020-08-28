<properties
    pageTitle="Portal, Client Tools and APIs"
    description="Portal, Client Tools and APIs"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747576"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-gen1-portalclient-powershell"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Portal, Client Tools and APIs - Setting up Monitoring and Alerts
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "MySQL Powershell scoping questions",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "command",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which command(s) are you experiencing issues with?",
            "required": false
        },
        {
            "id": "same_issue_server",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "If you have multiple servers, did you experience the same issue on other servers?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
