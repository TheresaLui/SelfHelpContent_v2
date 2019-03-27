<properties
	articleId="Cloudyn-problemscopingquestions"
	pageTitle="Cloudyn Legacy"
	description="Cloudyn Legacy"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32615277,32615279,32615288,32615289,32615290,32615291,32615292,32615294,32615295,32615296,32615299,32615300,32615301,32615302,32615303,32615304,32615305"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Cloudyn Legacy
---
{
    "resourceRequired": true,
    "title": "Cloudyn Legacy",
    "fileAttachmentHint": "",
    "formElements": [
	     {
	            "id": "problem_start_time",
	            "order": 1,
	            "controlType": "datetimepicker",
	            "displayLabel": "Problem start time",
	            "required": true
	        },
           {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide any additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Describe your issue in detail"
                }
            ]
        }
       ]
}
---
