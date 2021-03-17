<properties 
  pageTitle="Always On Availability Groups- Configuration"
  description="Always On Availability Groups- Configuration"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740063"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="9a0f4e76-92d0-443e-b96c-99f8d63945bc"
 ownershipId="AzureData_AzureSQLVM"
/>
# Always On Availability Groups- Configuration
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Always On Availability Groups- Configuration",
    "fileAttachmentHint": null,
    "diagnosticCard": {
    "title": "Setup Availability Group Troubleshooter",
    "description": "Our Setup Availability Group Troubleshooter can help you troubleshoot and solve your problem.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "which_resource",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What resource do you need assistance configuring?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Availability Group",
                    "value": "AvailabilityGroup"
                },
                {
                    "text": "Availability Group Listener",
                    "value": "AvailabilityGroupListener"
                },
                {
                    "text": "Failover Cluster settings",
                    "value": "FailoverClusterSettings"
                },
                {
                    "text": "Configure Read Only Routing",
                    "value": "AvailabilityGroupRouting"
                },
                {
                    "text": "Add a new replica",
                    "value": "FailoverClusterSettings"
                },
                {
                    "text": "Add a database to an Availability Group",
                    "value": "FailoverClusterSettings"
                },
                {
                    "text": "Other resource",
                    "value": "OtherResource"
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
            "id": "how_far_in_configuration",
            "visibility": "which_resource != dont_know_answer",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How far along are you in making the configuration change?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "I'm still planning and have questions",
                    "value": "StillPlanning"
                },
                {
                    "text": "I've already started and have encountered a problem",
                    "value": "ProblemEncountered"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "method_of_configuration",
            "visibility": "how_far_in_configuration != null && how_far_in_configuration == ProblemEncountered",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What method are you using to make the configuration change?",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure Portal",
                    "value": "Portal"
                },
                {
                    "text": "Quickstart template",
                    "value": "QuickstartTemplate"
                },
                {
                    "text": "Azure CLI",
                    "value": "Cli"
                },
                {
                    "text": "Powershell",
                    "value": "Powershell"
                },
                {
                    "text": "Transact-SQL",
                    "value": "Tsql"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "ag_listener_problem",
            "visibility": " which_resource == AvailabilityGroupListener",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is not working with the Listener?",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Initial configuration",
                    "value": "InitialConfiguration"
                },
                {
                    "text": "Connectivity",
                    "value": "Connectivity"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "resource_name",
            "order": 6,
            "visibility": " which_resource != dont_know_answer && how_far_in_configuration != null && how_far_in_configuration == ProblemEncountered",
            "controlType": "multilinetextbox",
            "displayLabel": "Name of the resource",
            "watermarkText": "Provide the name of the resource you're having problems with",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "issue_type",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Choose an option that best describes your Availability Group setup issue.",
            "watermarkText": "Common Setup Availability Group issue categories",
            "infoBalloonText": "Setup Availability Group issue category",
            "dropdownOptions": [
            {
            "value": "AvailabilityGroupsConfiguration_Procedure",
            "text": "Procedure to Configure Availability Groups"
            },
            {
            "value": "AvailabilityGroupsConfiguration_AcrossRegions_Or_DisasterRecoverySite",
            "text": "Configure Availability Group across different regions or as a Disaster Recovery Site"
            },
            {
            "value": "AvailabilityGroupsConfiguration_CommonErrors",
            "text": "Common Errors encountered while Configuring Availability Groups"
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
            "value": "AvailabilityGroupsConfiguration_DistributedAvailabilityGroup_DAG",
            "text": "Configure Distributed Availability Group (DAG)"
            },
            {
            "value": "dont_know_answer",
            "text": "None of the above"
            }
        ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
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
