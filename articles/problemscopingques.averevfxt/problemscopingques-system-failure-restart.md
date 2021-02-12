<properties
	pageTitle="Avere vFXT System Failure or Service Restart"
	description="System Failure or Service Restart"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32609696"
	productPesIds="16506"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="50d10e1e-9167-483c-935b-f12448375f8a"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>
# Problems involving a system failure or service restart.
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Problems involving a system failure or service restart",
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
        "id": "avere_alert_text",
        "order": 3,
        "controlType": "multilinetextbox",
        "displayLabel": "Alert Text",
        "watermarkText": "Alert text from management interface",
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
