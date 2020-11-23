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
    "description": "Our Setup Availability Group Troubleshooter can help you troubleshoot and solve your problem."
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
                    "text": "AG failed or failed over or did not failover",
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
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        }
    ],
    "$schema": "SelfHelpContent"
}
---