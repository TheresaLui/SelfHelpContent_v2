<properties
	pageTitle="MSIX app attach issues"
	description="MSIX app attach issues"
	ms.author="jerrycif"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32784012,32784013"
	productPesIds="16582"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="fb177db5-4368-4448-9fc5-d047a70fd2bd"
	ownershipId="Windows_Virtual_Desktop"
/>
# MSIX app attach
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "MSIX app attach",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_description",
      "order": 1,
      "controlType": "multilinetextbox",
      "displayLabel": "Details",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Issue description."
        },
        {
          "text": "Name of the session host or virtual machines"
        }
      ]
    },
    {
      "id": "error message",
      "order": 2,
      "controlType": "dropdown",
      "infoBalloonText": "string",
      "displayLabel": "Are there any error messages displayed?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't Know"
        }
      ],
      "required": false
    },
    {
      "id": "what error",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the exact error you see",
      "watermarkText": "Please specify the exact issue that occurred",
      "required": true
    },
    {
      "id": "problem_start_time",
      "order": 4,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    },
    {
      "id": "impact",
      "order": 5,
      "controlType": "multiselectdropdown",
      "displayLabel": "Who is impacted by the issue",
      "dropdownOptions": [
        {
          "value": "A single user",
          "text": "A single user"
        },
        {
          "value": "Multiple users",
          "text": "Multiple users"
        },
        {
          "value": "All users",
          "text": "All users"
        },
        {
          "value": "I don't know",
          "text": "I don't know"

        }
      ],
      "required": false
    },
    {
      "id": "how often",
      "order": 6,
      "controlType": "multiselectdropdown",
      "displayLabel": "How often does this issue occur",
      "dropdownOptions": [
        {
          "value": "Daily",
          "text": "Daily"
        },
        {
          "value": "Intermittent",
          "text": "Intermittent"
        },
        {
          "value": "I can replicate at will",
          "text": "I can replicate at will"
        },
        {
          "value": "I don't know",
          "text": "I don't know"
        }
      ]
    }
  ]
}
---
