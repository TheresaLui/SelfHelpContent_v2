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
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
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
      "controlType": "multiselectdropdown",
      "displayLabel": "Which route is having issues?",
      "watermarkText": "Choose an option",
      "dynamicDropdownOptions": {
        "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Devices/IotHubs/{resourcename}?api-version=2018-04-01",
        "jTokenPath": "properties.routing.routes",
        "textProperty": "name",
        "valueProperty": "name",
        "textPropertyRegex": "[^/]+$",
        "defaultDropdownOptions": {
          "value": "dont_know_answer",
          "text": "Other, don't know, or not applicable"
        }
      },
      "dropdownOptions": [{
        "value": "no_route",
        "text": "Could not find any routes in this hub"
      }],
      "required": true
    },
    {
      "id": "endpoint",
      "order": 3,
      "visibility": "route_name != null && route_name != no_route && route_name != dont_know_answer",
      "controlType": "dropdown",
      "displayLabel": "Endpoint",
      "watermarkText": "Choose an option",
      "dynamicDropdownOptions": {
        "dependsOn": "route_name",
        "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Devices/IotHubs/{resourcename}?api-version=2018-04-01",
        "jTokenPath": "properties.routing.routes[?(@.name == '{replaceWithParentValue}')]",
        "textProperty": "endpointNames",
        "valueProperty": "endpointNames",
        "valuePropertyRegex": "[^/]+$"
      },
      "dropdownOptions": [{
        "value": "no_endpoint",
        "text": "Could not find an endpoint associated to this route"
      }],      
      "required": true
    },
    {
      "id": "problem_description",
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "Details and error logs",
      "watermarkText": "Provide additional information and logs",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [{
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