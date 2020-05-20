<properties
	pageTitle="Avere vFXT Upgrade Assistance Request"
	description="Upgrade Assistance Request"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32609697"
	productPesIds="16506"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="99351f36-63b1-45ee-bb58-b21654f802f2"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>
# Upgrade Assistance Request
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Upgrade Assistance Request",
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
        "displayLabel": "Current Avere OS Version",
        "watermarkText": "Version Number",
        "required": false
    }, {
        "id": "avere_target_os_version",
        "order": 3,
        "controlType": "textbox",
        "displayLabel": "Target Avere OS Version",
        "watermarkText": "Version Number",
        "required": false
    }, {
        "id": "avere_upgrade_time_info",
        "order": 4,
        "controlType": "infoblock",
        "content": "If you have a planned date and time for the upgrade, please enter it below."
    }, {
        "id": "avere_upgrade_date_time",
        "order": 5,
        "controlType": "datetimepicker",
        "displayLabel": "Upgrade Date and Time",
        "watermarkText": "Date and Time",
        "required": false
    }, {
        "id": "problem_description",
        "order": 6,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 7,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
