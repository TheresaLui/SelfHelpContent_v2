 <properties
      articleId="A8F9AC37-12CB-4DA5-B89C-E3D19311E5BD"
      pageTitle="create automation account or schedule runbook"
      description="create automation account or schedule runbook"
      authors="pjfreitas"
      ms.author="pfreitas"
      selfHelpType="problemScopingQuestions"
      supportTopicIds="32675695"
      productPesIds="16157"
      cloudEnvironments="public, MoonCake, fairfax, usnat, ussec" 
      schemaVersion="1"
	ownershipId="AzureData_AnalysisServices"
/>
# Create a standalone Azure Automation account
---
{
  "resourceRequired": false,
  "subscriptionRequired": true,
  "title": "Create a standalone Azure Automation account",
  "fileAttachmentHint":"",
  "formElements":
  [
    {
      "id": "problem_description",
      "order": 100,
      "controlType": "multilinetextbox",
      "displayLabel": "Additional details about the issue",
      "watermarkText": "The attempted scenario with resulting observed vs expected behavior.",
      "required": true,
      "useAsAdditionalDetails": true
    }
,
    {
      "id": "problem_start_time",
      "order": 200,
      "controlType": "datetimepicker",
      "displayLabel": "What time did the problem begin?",
      "required": true
    }
,
    {
      "id": "problem_end_time",
      "order": 300,
      "controlType": "datetimepicker",
      "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
      "required": false
    }
,
    {
      "id": "create_automation_account_or_schedule_runbook_400",
      "order": 400,
      "controltype": "dropdown",
      "displaylabel": "Has this automation worked previously? ",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "create_automation_account_or_schedule_runbook_500",
      "order": 500,
      "controltype": "dropdown",
      "displaylabel": "Do you have other automations currently running without issue?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "create_automation_account_or_schedule_runbook_600",
      "order": 600,
      "controltype": "multilinetextbox",
      "displaylabel": "What is the full error message with all error IDs?",
      "watermarktext": "What is the full error message with all error IDs?",
      "required": false
    }
,
    {
      "id": "create_automation_account_or_schedule_runbook_700",
      "order": 700,
      "controltype": "dropdown",
      "displaylabel": "Can the issue be reproduced by other users?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "create_automation_account_or_schedule_runbook_800",
      "order": 800,
      "controltype": "multilinetextbox",
      "displaylabel": "Is this an intermittent or permanent issue?",
      "watermarktext": "Is this an intermittent or permanent issue?",
      "required": false
    }
  ],
  "$schema": "SelfHelpContent"
}
---
