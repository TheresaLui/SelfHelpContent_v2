<properties
	pageTitle="Azure Sentinel - Workbooks  - Issues with workbooks templates "
	description="Azure Sentinel - Workbooks  - Issues with workbooks templates "
	authors="yaronsahar-ms"
	ms.author="yaronsahar"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32786027"
    productPesIds="16690"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping-issues-with-workbooks-templates"
	schemaVersion="1"
	ownershipId="Azure_Sentinel"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Issues with workbooks templates ",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Please provide any screenshots that are relevant to your issue",
				"formElements": [{
                "id": "WorkbookName",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "What is the Workbook name?",
                "required": true
                },{
				"id": "problem_description",
				"order": 1,
				"controlType": "multilinetextbox",
				"displayLabel": "Description",
				"useAsAdditionalDetails": true,
				"required": true
				},{
				"id": "problem_start_time",
				"order": 8,
				"controlType": "datetimepicker",
				"displayLabel": "When did the problem start?",
				"required": true
                  }]
}
---