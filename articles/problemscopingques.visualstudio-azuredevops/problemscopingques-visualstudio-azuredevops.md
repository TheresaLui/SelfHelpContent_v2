<properties
	
	articleId="problemscopingques-visualstudio-azuredevops"
	pageTitle="Scoping questions for Azure DevOps Issues"
	description="Scoping questions for Azure DevOps Issues"
	authors="chrisjco"
	ms.author="ccoop"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="
32542242,
32572375,
32612983,
32612984,
32260182,
32260185,
32260188,
32300884,
32453003,
32260219,
32260215,
32453004,
32612992,
32452978,
32452987,
32452990,
32452992,
32260177,
32404472,
32452997,
32572844,
32300879,
32612985,
32277578,
32452998,
32260176,
32588005,
32608800,
32588006,
32588007,
32452969,
32452991,
32452979,
32452980,
32452983,
32452985,
32572358,
32612986,
32572359,
32572364,
32452970,
32452971,
32452982,
32452986,
32452989,
32452995,
32572360,
32572361,
32572362,
32572363,
32612991,
32260186,
32453000,
32453001,
32260203,
32453002,
32510202,
32260183,
32260213,
32260218,
32542243,
32542241,
32452996,
32572366,
32572368,
32572367,
32572369,
32572370,
32572371,
32542238,
32452976,
32542244,
32452993,
32452994"

	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Azure_DevOps_Services"

/>
# Azure DevOps Issues
---
{
"$schema": "SelfHelpContent",
"resourceRequired": false,
  "subscriptionRequired": false,
  "title": "Azure DevOps Issues",
    "fileAttachmentHint": "Please upload any screenshots or relevant logs",
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
          "text": "Screenshots or Logs"
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
      "id": "project_name",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Please provide the name of Team Project affected",
      "required": false
    },
    {
      "id": "problem_start_time",
      "order": 4,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    }
  ]
}
---