<properties 
  pageTitle="Crash or unexpected termination in package execution"
  description="Crash or unexpected termination in package execution"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32749435"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="6afed1d3-7118-4bf6-9bb3-62a532d0693d"
  ownershipId="AzureData_AzureSQLVM"
/>
# Crash or unexpected termination in package execution
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Crash or unexpected termination in package execution",
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
         "id": "whatCrashes",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Is there an application that is crashing or is an SSIS Package failing with Unexpected Termination?",
            "content": null,
            "infoBalloonText": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
         {
         "id": "hasWorked",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the version of Visual Studio SSDT and SSIS Runtime being used??",
            "content": null,
            "infoBalloonText": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "VS",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "If Visual Studio SSDT is crashing, when is the crash happening? ",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "While opening the package in Visual Studio SSDT",
                    "value": "Open"
                },
                {
                    "text": "While designing the package",
                    "value": "Design"
                },
                {
                    "value": "While executing the package.",
                    "text": "Execute"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "issueType",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are any 3rd party components or custom tasks or .NET assemblies a part of the package design?",
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
                    "value": "dont_know_answer",
                    "text": "I'm not sure/don't know"
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
