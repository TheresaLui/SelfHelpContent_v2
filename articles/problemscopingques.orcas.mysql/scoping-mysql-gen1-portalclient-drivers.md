<properties
    pageTitle="Portal, Client Tools and APIs"
    description="Portal, Client Tools and APIs"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747551"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-gen1-portalclient-drivers"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Portal, Client Tools and APIs - Setting up Monitoring and Alerts
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "MySQL Driver Scoping Questions",
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
            "id": "drivers",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which driver or APIs are you using?",
            "required": false
        },
        {
            "id": "version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which version of driver or APIs are you using?",
            "required": false
        },
        {
            "id": "error_message",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Which error message thrown from driver or APIs?",
            "required": false
        },
        {
            "id": "same_issue_server",
            "order": 5,
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
            "order": 6,
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
