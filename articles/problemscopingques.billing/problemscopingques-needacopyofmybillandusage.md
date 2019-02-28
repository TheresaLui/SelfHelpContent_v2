<properties
	pageTitle="Request a Copy of My Bill and Usage"
	description="Request a Copy of My Bill and Usage"
	articleId="requestacopyofmybillandusage"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454862"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Request a Copy of My Bill and Usage
---
{
  "resourceRequired": false,
  "title": "Request a Copy of My Bill and Usage",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "visibility": null,
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "Problem Start Date",
      "required": true
    },
    {
      "id": "emailid_details",
      "order": 2,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Email ID used to download report",
      "watermarkText": "Provide the Email ID used to download report",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Error message (if applicable)",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Describe your problem, providing as much detail as possible."
        }
      ]
    }
  ]
}

---
