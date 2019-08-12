<properties
	pageTitle="Routing issues"
	description="Routing issues for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680884,32680885"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	schemaVersion="1"
	articleId="53fe32ef-1e90-4ff9-943d-8b55e8abb4bc"
/>
# Routing issues
---{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": true,
  "title": "Routing issues",
  "fileAttachmentHint": "Upload screenshots of errors if available",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
        "id": "route_name",
        "order": 2,
        "controlType": "dropdown",
        "displayLabel": "Which route is having issues?",
        "watermarkText": "Choose an option",
        "dynamicDropdownOptions": {
            "uri": "{resourceId}?api-version=2018-12-01-preview",
            "jTokenPath": "$.properties.routing.routes",
            "textProperty": "name",
            "valueProperty": "name",
            "textPropertyRegex": "[^/]+$",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know, or not applicable"
            }            
        },
        "dropdownOptions": [
            {
                "value": "Could not find any routes in this hub",
                "text": "Could not find any routes in this hub"
            }
        ],
        "required": false
    },
    {
      "id": "problem_description",
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "Details and error logs",
      "watermarkText": "Provide additional information and logs",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Error logs with timestamp (indicate timezone or UTC)"
        },
        {
          "text": "Any other details"
        }
      ]
    }
  ]
}
---