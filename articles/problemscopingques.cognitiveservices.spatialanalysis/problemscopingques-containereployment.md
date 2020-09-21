<properties
  articleId="235288f0-b30e-f736-5221-0d4b6323680f"
  pageTitle="Scoping questions - Issues related to spatial analysis usage"
  description="Scoping questions to troubleshoot the issues related to the container deployment for spatial analysis."
  authors="kabrow"
  authoralias="kabrow"
  ms.author="kabrow"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32767687"
  productPesIds="16970" 
  cloudEnvironments="public, Fairfax, usnat, ussec, mooncake"
  schemaVersion="1"
  ownershipId="AzureCogSvc_CognitiveServices"
/>

# Issues related to the container deployment for spatial analysis
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Issues related to the spatial analyssis container deployment",
  "fileAttachmentHint": "Are you able to gather any log information using the following commands:
  	• Container logs:
		○ sudo iotedge logs <your-container-name>
	• Logs of the security manager:
		○ sudo journalctl -u iotedge -f
	• Comprehensive system logs:
		○ sudo iotedge support-bundle --since 6h
  What is the status of your containers when you run: 
	• sudo systemctl status iotedge
Attach the results of your logs."
  ",

  "formElements": [
{
      "id": "container_version",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What version is your container? Have you tried updating your container version and re-deploying?",
      "useAsAdditionalDetails": true,
      "required": true
    }

    {
      "id": "deployment_method",
      "order": 3,
       "controlType": "radiobuttongroup",
      "displayLabel": "What method are you using to deploy the container?",
      "radioButtonOptions": [
        {
          "value": "CLI",
          "text": "The Azure CLI"
        },
        {
          "value": "Portal",
          "text": "The Azure Portal"
        }
      ],
      "required": true
    },

    {
      "id": "sample_module",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Did you try deploying a sample module and were you successful?",
      "useAsAdditionalDetails": true,
      "required": true
    }

    {
      "id": "problem_description",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Problem description",
      "watermarkText": "Can you provide any additional details about the issue you are having regarding your container deployment?",
      "useAsAdditionalDetails": true,
      "required": false
    }
  ]
}
---