<properties pageTitle="Cannot Connect to SQL Instance"
  description="Cannot Connect to SQL Instance"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740109"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="af5b32e5-3760-442b-8a81-65fb35a1a5d0"
 ownershipId="AzureData_AzureSQLVM"
/>
# Cannot Connect to SQL Instance
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cannot Connect to SQL Instance",
    "fileAttachmentHint": null,
	"diagnosticCard": {
    "title": "Cannot connect to SQL Instance Troubleshooter",
    "description": "Cannot connect to SQL Instance Troubleshooter can help you troubleshoot and solve your problem.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
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
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "issue_type",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Choose an option that best describes your Cannot connect to SQL Instance issue.",
            "watermarkText": "Common Cannot connect to SQL Instance categories",
            "infoBalloonText": "Cannot connect to SQL Instance issue category",
            "dropdownOptions": [
            {
            "value": "CannotConnectToSQLInstance",
            "text": "Cannot Connect to SQL instance"
            },

            {
            "value": "AvailabilityGroupsConfiguration_SetupListenerAndLoadBalancer",
            "text": "Setup Listener and Load Balancer for Availability Groups"
            },
            {
            "value": "AvailabilityGroupsConfiguration_Listener_ConnectivityIssue",
            "text": "Configured Availability Group but Unable to connect using Listener"
            },

            {
            "value": "dont_know_answer",
            "text": "None of the above"
            }
        ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        }
    ]
}
---
