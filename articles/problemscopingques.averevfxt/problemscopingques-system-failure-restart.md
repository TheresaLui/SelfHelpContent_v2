<properties
	pageTitle="Avere vFXT System Failure or Service Restart"
	description="System Failure or Service Restart"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32609696"
	productPesIds="16506"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="50d10e1e-9167-483c-935b-f12448375f8a"
/>
# Problems involving a system failure or service restart.
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "diagnosticCard": {
        "title": "Avere vFXT Cluster Name",
        "description": "Provide the Avere OS version that is running.",
        "id": "avere_cluster_name",
        "order": 1,
        "controlType": "textbox",
        "displayLabel": "Avere vFXT Cluster Name",
        "watermarkText": "Cluster Name",
        "required": false
    }
    "diagnosticCard": {
        "title": "Avere OS Version",
        "description": "Provide the Avere OS version that is running.",
        "id": "avere_os_version",
        "order": 2,
        "controlType": "textbox",
        "displayLabel": "Avere OS Version",
        "watermarkText": "Version Number",
        "required": false
    }
    "diagnosticCard": {
        "title": "Alert Text",
        "description": "Alert text from the management interface regarding the failure.",
        "id": "avere_alert_text",
        "order": 3,
        "controlType": "multilinetextbox",
        "displayLabel": "Alert Text",
        "watermarkText": "Alert text from management interface",
        "required": false
    }
}
---
