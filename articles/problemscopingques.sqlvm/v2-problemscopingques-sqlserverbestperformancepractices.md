<properties 
  pageTitle="SQL Server Performance Best Practices"
  description="SQL Server Performance Best Practices"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740099"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="e29ba5c3-a0d2-47dd-a021-2f37a4f1e360"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server Performance Best Practices
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Server Performance Best Practices",
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
            "id": "whatPractices",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you implemented the best practices for SQL Server on azure VM?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "I am facing issues after implementing",
                    "value": "IAmFacingIssuesAfterImplementing"
                },
                {
                    "text": "I need help configuring it or have questions",
                    "value": "INeedHelpConfiguringItOrHaveQuestions"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I'm not sure/don't know"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
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
