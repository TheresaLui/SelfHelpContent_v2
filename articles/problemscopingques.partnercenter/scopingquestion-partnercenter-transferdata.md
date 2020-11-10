<properties
	pageTitle="Partner Center Transfer Data"
	description="Partner Center Transfer Data"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725884"
	productPesIds="17012"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_transferdata"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Transact_and_Manage"
/>
# Partner Center Transfer Data
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Transfer Data",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_customerfrom_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer tenant ID (GUID) you are transfering from",
            "watermarkText": "Customer tenant ID transfering from",
            "required": false
        },
 	{
            "id": "pc_customerto_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer tenant ID (GUID) you are transfering to",
            "watermarkText": "Customer tenant ID transfering to",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
