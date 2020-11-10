<properties
  pageTitle="VM Size guidelines"
  description="VM Size guidelines"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740115"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT" 
  schemaVersion="1"
  articleId="3b56d27e-be8e-4ea4-9e38-cc21a28c37d9"
  ownershipId="AzureData_AzureSQLVM"
/>
# VM Size guidelines 
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My desired region or VM size is unavailable",
    "fileAttachmentHint": "",
    "diagnosticCard": {
      "title": "Virtual machine deployment diagnostics",
      "description": "These diagnostics will check for details about your selected deployment failure.",
      "insightNotAvailableText": "We didn't find any problems"},
      "formElements": [
          {
            "id": "resourceGroup",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select resource group for deployment failure",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of resource groups.",
                    "text": "Unable to retrieve list of resource groups."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "correlationId",
            "order": 2,
            "visibility": "resourceGroup != null && resourceGroup != dont_know_answer",
            "controlType": "dropdown",
            "displayLabel": "Select failed deployment",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/resourcegroups/{replaceWithParentValue}/providers/Microsoft.Resources/deployments/?api-version=2018-05-01&$filter=provisioningState%20eq%20'Failed'&$top=10",
                "jTokenPath": "value",
                "textProperty": "properties.timestamp,properties.parameters.location.value,name",
                "textTemplate": "Time:{properties.timestamp} Region:{properties.parameters.location.value} Name:{name}",
                "valueProperty": "properties.correlationId",
                "defaultDropdownOptions": {
                    "value": "Deployment failure not found.",
                    "text": "Deployment failure not found."
                },
                "textPropertyRegex": "[^/]+$",
                "valuePropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of failed deployments.",
                    "text": "Unable to retrieve list of failed deployments."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "deployment_size",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the size of the VM you are trying to deploy?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "deployment_isinavailabilitysetzone",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying your VM in an availability set or zone?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
