 <properties
      articleId="9F5E5B57-F404-4967-84F7-CB865518D3D4"
      pageTitle="subscription"
      description="subscription"
      authors="pjfreitas"
      ms.author="pfreitas"
      selfHelpType="problemScopingQuestions"
      supportTopicIds="32675699"
      productPesIds="16157"
      cloudEnvironments="public, MoonCake, fairfax, usnat, ussec" 
      schemaVersion="1"
	ownershipId="AzureData_AnalysisServices"
/>
# Organizing subscriptions and resource groups within the Enterprise
---
{
  "resourceRequired": false,
  "subscriptionRequired": true,
  "title": "Organizing subscriptions and resource groups within the Enterprise",
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
      "id": "subscription_400",
      "order": 400,
      "controltype": "dropdown",
      "displaylabel": "Are you a subscription administrator?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, dont know or not applicable"}],
      "required": true
    }
,
    {
      "id": "subscription_500",
      "order": 500,
      "controltype": "dropdown",
      "displaylabel": "Can the issue be reproduced by other administrators?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "subscription_600",
      "order": 600,
      "controltype": "multilinetextbox",
      "displaylabel": "What is the full error message with all error IDs?",
      "watermarktext": "What is the full error message with all error IDs?",
      "required": false
    }
,
    {
      "id": "subscription_700",
      "order": 700,
      "controltype": "dropdown",
      "displaylabel": "Can the issue be reproduced by other users?",
      "watermarkText":"Choose an option","dropdownOptions":[{"value": "Yes","text": "Yes"},{"value": "No","text": "No"},{"value": "dont_know_answer","text":"Other, don't know or not applicable"}],
      "required": true
    }
,
    {
      "id": "subscription_800",
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
