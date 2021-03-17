<properties 
  pageTitle="Always On Availability Groups- Manage or Troubleshoot"
  description="Always On Availability Groups- Manage or Troubleshoot"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740064"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="76d94a7d-a601-4c55-a728-08579cc8eea1"
  ownershipId="AzureData_AzureSQLVM"
/>
# Always On Availability Groups- Manage or Troubleshoot
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Always On Availability Groups- Manage or Troubleshoot",
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
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "which_resource",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What area do you need assistance troubleshooting?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "AG failed or failed over or did not fail over",
                    "value": "AvailabilityGroupFailovers"
                },
                {
                    "text": "Listener Connectivity",
                    "value": "ListenerConnectivity"
                },
                {
                    "text": "Database in Not Synchronizing or in Recovery Pending Mode",
                    "value": "DatabaseState"
                },
                {
                    "text": "Redo Rate is slow",
                    "value": "RedoRate"
                },
                {
                    "text": "Availability Group performance",
                    "value": "AGPerformance"
                },
                {
                    "text": "AG Resource failures(Listener/IP does not come online, AG is in failed state)",
                    "value": "AGResourceFailures"
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
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Choose an option that best describes AG failure,failover,sync issue.",
            "watermarkText": "Common Setup Availability Group issue categories",
            "infoBalloonText": "Availability Group Failure, Failover, Sync issue",
            "dropdownOptions": [
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_Timeout",
                    "text": "AG failed/restarted/failedover/leasetimeout happened"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_AGOffline_Or_DB_Resolving_State",
                    "text": "AG is offline or databases are in resolving state"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_AGSlow",
                    "text": "AG is slow to synchronize or redo is lagging"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_Why_AG_Did_Not_Failover",
                    "text": "Why AG did not failover?"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_Unable_Failover_AG_Another_Replica",
                    "text": "Unable to failover AG"
                },
                {
                    "value": "AvailabilityGroupsFailure_UnableToConnect_Listener",
                    "text": "Unable to connect to AG listener"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_Unableto_Login_After_Failover",
                    "text": "Unable to login after failover"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_Misaligned_LogIOs",
                    "text": "There have been X misaligned log IOs"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_AGDBLog",
                    "text": "AG db log file is growing or unable to shrink"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_How_Do_I_Setup_AG",
                    "text": "How do I setup AG"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_EventID_1135",
                    "text": "Quorum lost/Windows cluster stops/EventId 1135-Node was removed"
                },
                {
                    "value": "AvailabilityGroupFailure_Failover_SyncIssue_EventID_157",
                    "text": "EventId 157 - Disk was surprised removed"
                },
                {
                    "value": "dont_know_answer",
                    "text": "None of the above"
                }
        ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        }
    ],
    "$schema": "SelfHelpContent"
}
---