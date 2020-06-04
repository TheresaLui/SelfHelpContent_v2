<properties 
  pageTitle="SQL Server is Slow"
  description="SQL Server is Slow"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740098"
  productPesIds="14745"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="e8b21a94-2d67-4df1-9fcd-8c81f2457660"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server is Slow
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Server is Slow",
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
            "id": "whichPhase",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of SQL performance problem do you need assistance with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "All SQL Server operations are slow",
                    "value": "SQLServerSlow"
                },
                {
                    "text": "A specific query is slow",
                    "value": "QuerySlow"
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
            "id": "whichBaseline",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What baseline are you using to assess things are slow?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "It previously ran faster on this VM",
                    "value": "FasterBeforeSameVM"
                },
                {
                    "text": "It's faster on another environment that runs this workload (e.g., on-premise SQL instance)",
                    "value": "FasterDifferentEnvironment"
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
            "id": "statsRun",
            "visibility": "whichPhase == QuerySlow",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you run UPDATE STATISTICS WITH FULLSCAN on the table(s) being accessed by the query?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "No"
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
            "id": "queryProblem",
            "visibility": "whichPhase == QuerySlow",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Query",
            "watermarkText": " Please enter the text of the query you need assistance with.",
            "required": false,
            "useAsAdditionalDetails": false
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
