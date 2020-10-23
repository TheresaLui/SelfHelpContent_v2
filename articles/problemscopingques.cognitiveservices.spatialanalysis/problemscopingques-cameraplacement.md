<properties
  pageTitle="Scoping questions - Issues related to spatial analysis usage"
  description="Scoping questions to troubleshoot the issues related to the camera placement and configuration for spatial analysis."
  ms.author="kabrow"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32767685"
  productPesIds="16970"
  cloudEnvironments="public, Fairfax, usnat, ussec, mooncake"
  schemaVersion="1"
  articleId="fb58e668-32e6-3d93-7640-00ee727cc5b4"
  ownershipId="AzureCogSvc_CognitiveServices"
/>
# Issues related to camera placement and configuration for spatial analysis usage
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Issues related to the camera placement and configuration for the use of the spatial analysis container",
  "fileAttachmentHint": "Please provide a screenshot of any errors",
  "formElements": [{
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    },{
      "id": "required_params",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Does your camera meet the required specs for running spatial analysis? Is your camera capable or streaming at 15FPS and 1080p resolution? Does your camera support Real Time Streaming Protocol (RTSP) and H.264 encoding?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [{
      	"value": "Yes",
	"text": "Yes"
	}, {
	"value": "No",
	"text": "No"
	},{
	"value": "dont_know_answer",
	"text": "Unsure"
	}
	],
      "required": true
    },{
      "id": "camera_usage_scenario",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Is your camera mounted on a wall, ceiling, or other device?",
      "watermarkText": "Provide details below",
      "required": false
    },{
      "id": "problem_description",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Problem description",
      "watermarkText": "Can you provide any additional details about the issue you are having regarding placing and configuring your camera?",
      "useAsAdditionalDetails": true,
      "required": true
    }
  ]
}
---
