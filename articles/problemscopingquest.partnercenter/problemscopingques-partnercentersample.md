<properties
	pageTitle="Partner Center Sample Title"
	description="Partner Center Sample Description"
	authors="srinivabms"
	ms.author="srinivab"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32444666,32633819"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercentersample"
/>
# PC Sample
---
{
    "resourceRequired": true,
    "title": "Partner Center Sample Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_app_gw_url",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the URL you are using to access the PC Application Gateway.",
            "watermarkText": "Provide full URL such as http://www.contoso.com:8081/home.aspx",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Details of the issue.",
            "watermarkText": "Provide additional information about your issue including error messages.",
            "required": true
        },
        {
            "id": "pc_learn_more_text",
            "order": 4,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/application-gateway/'>Learn more</a> about Application Gateway, including How to setup and troubleshooting steps."
        }
    ]
}
---
