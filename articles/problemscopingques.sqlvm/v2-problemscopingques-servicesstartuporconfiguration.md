<properties 
  pageTitle="Service startup or configuration"
  description="Service startup or configuration"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740089"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="1e11d0b3-87df-4f1b-8e96-1fe7fe8d3ec8"
  ownershipId="AzureData_AzureSQLVM"
/>
# Service startup or configuration
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Service startup or configuration",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "whichService",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What service do you need help with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "SQL Server Service",
                    "value": "SQLServerService"
                },
                {
                    "text": "SQL Server Agent",
                    "value": "SQLServerAgent"
                },
                {
                    "text": "Browser Service",
                    "value": "BrowserService"
                },
                {
                    "text": "SQL Server VSS Writer",
                    "value": "VSSWriter"
                },
                {
                    "text": "I'm not sure/don't know",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
             "id": "WhyFails",
             "visibility": "whichService == SQLServerService",
             "order": 3,
             "controlType": "dropdown",
             "displayLabel": "SQL Service is not starting after:",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "I applied SQL or a Windows patch",
                     "value": "AppliedPatch"
                 },
                 {
                     "text": "Changed service account, moved database files",
                     "value": "ChangedConfig"
                 },
                 {
                     "text": "Post VM restarted",
                     "value": "VMRestarted"
                 },
                 {
                     "text": "Encountered certificate error",
                     "value": "CertificateError"
                 },
                 {
                     "text": "I'm not sure/don't know",
                     "value": "dont_know_answer"
                 }
             ],
             "dynamicDropdownOptions": null,
             "required": false,
             "maxLength": 0,
             "useAsAdditionalDetails": false,
             "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
