<properties
    pageTitle="Server Parameters"
    description="Server Parameters"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747550"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-gen1-server-parameter_notlisted"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Server Parameters - Server parameter not listed
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Server Parameters Not Listed",
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
            "id": "server_parameter",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What server parameter(s) do you want to change?",
            "required": false
        },
        {
            "id": "parameter_scenario",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What scenario the parameter(s) is used for",
            "watermarkText": "Provide your scenario",
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
