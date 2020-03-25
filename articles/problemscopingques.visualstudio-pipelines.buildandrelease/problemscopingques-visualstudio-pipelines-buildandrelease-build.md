<properties
	articleId="problemscopingques-visualstudio-pipelines-buildandrelease-build"
	pageTitle="Scoping questions for Pipelines Build Issues"
	description="Scoping questions for Pipelines Build Issues"
	authors="chrisjco"
	ms.author="ccoop"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32452973, 32452974, 32572374, 32572376, 32572373"
	productPesIds="15543"
	cloudEnvironments="public"
	schemaVersion="1"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# Pipelines Issues Build
---
{
"$schema": "SelfHelpContent",
"resourceRequired": false,
  "subscriptionRequired": false,
  "title": "Pipeline Issues",
    "fileAttachmentHint": "Upload any screenshots or the <a href='https://docs.microsoft.com/azure/devops/pipelines/troubleshooting?view=azure-devops#get-logs-to-diagnose-problems'>Diagnostic log</a>",
  "formElements": [
    {
      "id": "problem_description",
      "order": 1,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide these details",
      "required": true,
      "watermarkText": "Please provide: a detailed scenario of the error condition or issue, troubleshooting done so far, and any other relevant information.",
      "useAsAdditionalDetails": true,
      "hints": [
      	{
          "text": "Error message (if any)"
        },
	{
          "text": "Troubleshooting done so far"
        },
        {
          "text": "Additional details"
        },
        {
          "text": "Screenshots and Diagnostic log"
        }
      ]
    },
    {
      "id": "org_name",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Please provide your Azure DevOps Organization URL (like XYZ.visualstudio.com or dev.azure.com/XYZ)",
      "watermarkText": "Organization URL",
      "required": false
    },
    {
      "id": "definition_name",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Name of pipeline affected",
      "required": false
    },
    {
      "id": "project_name",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "Name of Team Project with pipeline affected",
      "required": false
    },
    {
      "id": "problem_start_time",
      "order": 5,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    }
  ]
}
---
