<properties
	pageTitle="Issues with Container Registry SQL MIAA"
	description="Issues with Container Registry SQL MIAA"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743983"
	productPesIds="17125"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="1703a48d-f46a-440b-95f5-f4d66ec6fa6e"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Issues with Container Registry SQL MIAA
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "SQL Server - Azure Arc",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "container_registry_source",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "What container registry is your system configured to use?\n Use 'Use azdata arc dc config show |grep registry' to obtain",
			"required": false
		}, {
			"id": "error_message",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "What error message do you receive?",
			"required": false
		}, {
			"id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
