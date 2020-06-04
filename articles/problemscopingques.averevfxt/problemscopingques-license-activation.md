<properties
	pageTitle="Avere vFXT License Activation"
	description="License Activation Request"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32609692"
	productPesIds="16506"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="6717d922-bce8-47e3-9c14-bd88912dcbde"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>
# License Activation Request
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "License Activation Request",
    "formElements": [{
        "id": "avere_cluster_name",
        "order": 1,
        "controlType": "textbox",
        "displayLabel": "Avere vFXT Cluster Name",
        "watermarkText": "Cluster Name",
        "required": true
    }, {
        "id": "avere_os_version",
        "order": 2,
        "controlType": "textbox",
        "displayLabel": "Avere OS Version",
        "watermarkText": "Version Number",
        "required": false
    }, {
        "id": "avere_licensing_id",
        "order": 3,
        "controlType": "textbox",
        "displayLabel": "Avere Licensing ID",
        "watermarkText": "Licensing UUID",
        "required": false
    }, {
        "id": "problem_description",
        "order": 4,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 5,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
