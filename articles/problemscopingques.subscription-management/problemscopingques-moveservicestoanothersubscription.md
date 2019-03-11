<properties
	pageTitle="Move Services to Another Subscription"
	description="Move Services to Another Subscription"
	articleId="moveservicestoanothersubscription"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454926,32632956"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Move Services to Another Subscription
---
{
  "resourceRequired": false,
  "title": "Move Services to Another Subscription",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "Problem Start Date",
      "required": true
    },
    {
      "id": "sourcesubscriptionid_details",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Source (FROM) Subscription ID",
      "watermarkText": "Provide the Source (FROM) Subscription ID",
      "required": true
    },
    {
      "id": "destinationsubscriptionid_details",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Destination (TO) Subscription ID",
      "watermarkText": "Provide the Destination (TO) Subscription ID",
      "required": true
    },
    {
      "id": "services_details1",
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Move all Services or selective Services?",
      "watermarkText": "Move all Services or selective Services ",
      "dropdownOptions": [
        {
          "value": "All Services",
          "text": "All Services"
        },
        {
          "value": "Selective Services",
          "text": "Selective Services"
        }
      ],
      "required": true
    },
    {
      "id": "services_details2",
      "order": 5,
      "visibility": "services_details1 == Selective Services",
      "controlType": "multilinetextbox",
      "displayLabel": "Please list the services",
      "required": true
    },
    {
      "id": "requesterrole_details",
      "order": 6,
      "controlType": "dropdown",
      "displayLabel": "Requestor's current role assigned to the subscription",
      "watermarkText": "Select the Requestor's current role assigned to the subscription",
      "dropdownOptions": [
        {
          "value": "ARM",
          "text": "ARM"
        },
        {
          "value": "ASM",
          "text": "ASM"
        }
      ],
      "required": true
    },
    {
      "id": "problem_description",
      "order": 7,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Error message (if applicable)",
      "watermarkText": "Provide any error message or additional information about your issue",
      "required": true
    }
  ]
}
---
