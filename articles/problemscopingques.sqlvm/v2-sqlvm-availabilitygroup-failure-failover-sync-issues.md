<properties 
  pageTitle="Availability Group Failure, Failover, Sync issue"
  description="Availability Group Failure, Failover, Sync issue"
  authors="ujpat,amamun,babarmav"
  ms.author="ujpat,amamun,babarmav"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740064"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="d33e6b47-4101-441b-9f13-10553eb85ae9"
 ownershipId="AzureData_AzureSQLVM"
/>
# Availability Group Failure, Failover, Sync issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Availability Group Failure, Failover, Sync issue",
    "fileAttachmentHint": null,
    "diagnosticCard": {
    "title": "Availability Group Troubleshooter",
    "description": "Our Setup Availability Group Troubleshooter can help you troubleshoot and solve your problem.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
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
            "displayLabel": "Choose an option that best describes AG failure,failover,sync issue.",
            "watermarkText": "Common Setup Availability Group issue categories",
            "infoBalloonText": "Availability Group Failure, Failover, Sync issue",
            "dropdownOptions": [
            {
            "value": "AvailabilityGroupsFailure_LeaseTimeoutHappend",
            "text": "AG failed/restarted/failedover/leasetimeout happened"
            },
			{
            "value": "AvailabilityGroupsFailure_DB_ResolvingState",
            "text": "AG is offline or databases are in resolving state"
            },
			{
            "value": "AvailabilityGroupsFailure_SlowToSynchronize_OrRedoLagging",
            "text": "AG is slow to synchronize or redo is lagging"
            },
			{
            "value": "AvailabilityGroupsFailure_AG_DidNotFailover",
            "text": "Why AG did not failover?"
            },
			{
            "value": "AvailabilityGroupsFailure_UnableToFailuer_AnotherReplica",
            "text": "Unable to failover AG"
            },
            {
            "value": "AvailabilityGroupsFailure_UnableToConnect_Listener",
            "text": "Unable to connect to AG listener"
            },
			{
            "value": "AvailabilityGroupsFailure_UnableToLogin_AfterFailover",
            "text": "Unable to login after failover"
            },
			{
            "value": "AvailabilityGroupsFailure_Xmisaligned_LogIOs",
            "text": "There have been X misaligned log IOs"
            },
			{
            "value": "AvailabilityGroupsFailure_DBLogFileIssues",
            "text": "AG db log file is growing or unable to shrink"
            },
			{
            "value": "AvailabilityGroupsFailure_SetupAG",
            "text": "How do I setup AG"
            },
			{
            "value": "AvailabilityGroupsFailure_EventId_1135",
            "text": "Quorum lost/Windows cluster stops/EventId 1135-Node was removed"
            },
            {
            "value": "AvailabilityGroupsFailure_EventId_157",
            "text": "EventId 157 - Disk was surprised removed"
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