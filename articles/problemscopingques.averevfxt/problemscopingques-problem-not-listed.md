<properties
	pageTitle="Avere vFXT Problem Not Listed"
	description="My problem is not listed"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32609691"
	productPesIds="16506"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="8823dd45-57af-4dc1-8eaf-801f08edd3a8"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>
# My problem is not listed
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "My problem is not listed",
    "formElements": [{
        "id": "avere_cluster_name",
        "order": 1,
        "controlType": "textbox",
        "displayLabel": "Avere vFXT Cluster Name",
        "watermarkText": "Cluster Name",
        "required": false
    }, {
        "id": "avere_os_version",
        "order": 2,
        "controlType": "textbox",
        "displayLabel": "Avere OS Version",
        "watermarkText": "Version Number",
        "required": false
    }, {
        "id": "problem_description",
        "order": 3,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 4,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
