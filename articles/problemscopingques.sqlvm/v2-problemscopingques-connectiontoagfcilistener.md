<properties 
  pageTitle="Connection to Availability Groups, FCI, Listener"
  description="Connection to Availability Groups, FCI, Listener"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32782254"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="4c45fb54-74f6-45b3-8186-d11b1258a63b"
 ownershipId="AzureData_AzureSQLVM"
/>
# Connection to Availability Groups, FCI, Listener
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Connection to Availability Groups, FCI, Listener",
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
            "id": "connectivity_problem",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": " Is the connectivity issue consistent or intermittent?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Consistent (every time I try to connect)",
                    "value": "Consistent"
                },
                {
                    "text": "Intermittent (sometimes connections work)",
                    "value": "Intermittent"
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
            "id": "error_message",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Which error message are you encountering?",
            "watermarkText": "Provide the error message",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "source_of_connection",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the source of the connection?",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Locally, on the database server",
                    "value": "Local"
                },
                {
                    "text": "Another virtual machine in the same Azure VNET",
                    "value": "AnotherVmSameVnet"
                },
                {
                    "text": "Another virtual machine in Azure",
                    "value": "AnotherVmDiffVnet"
                },
                {
                    "text": "An Azure Web App",
                    "value": "AzureWebApp"
                },
                {
                    "text": "Outside of Azure(on-premise,other clouds)",
                    "value": "OnPremiseServer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "destination_of_connection",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the destination of the connection?",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "An Azure Virtual Machine with SQL Server installed (IaaS)",
                    "value": "AzureVm"
                },
                {
                    "text": "Azure SQL Database (PaaS)",
                    "value": "AzureSqlDb"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
             "id": "what_instance",
             "visibility": null,
             "order": 6,
             "controlType": "dropdown",
             "displayLabel": "What instance are you trying to connect to?",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "Default instance",
                     "value": "DefaultInstance"
                 },
                 {
                     "text": "Named Instance",
                     "value": "NamedInstance"
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
    ]
}
---
