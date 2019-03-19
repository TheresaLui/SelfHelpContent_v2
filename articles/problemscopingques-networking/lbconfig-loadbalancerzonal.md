<properties
	pageTitle="Configure a Zone-Specific Load Balancer"
	description="Configure a Zone-Specific Load Balancer"
	authors="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588976"
	productPesIds="16098"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId=""
/>
# SLB - Configure a Zone-Specific Load Balancer
---
{
 "resourceRequired": true,
 "title": "Configure a Zone-Specific Load Balancer",
 "fileAttachmentHint": "",
 "formElements": [
	 {
	 "id": "config_zonal_lb"
	 "order": 1,
	 "controlType": "dropdown",
	 "displayLabel": "Please select the Load Balancer resource type that you need help with",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Internal Load Balancer",
		 "text": "Internal Load Balancer"
		 },
		 {
		 "value": "Public Load Balancer",
		 "text": "Public Load Balancer"
		 },
	 ],
	 "required": true
	 },
	 {
		 "id": "problem_start_time",
		 "order": 2,
		 "controlType": "datetimepicker",
		 "displayLabel": "When did the problem begin?",
		 "required": false
	 },
	 {
		 "id": "problem_description",
		 "order": 5,
		 "controlType": "multilinetextbox",
		 "displayLabel": "Please specify any additional details or questions",
		 "required": false, 
		 "useAsAdditionalDetails": true,
		 "hints": [
			 {
			 "text": "Do you need help with any specific configuration problem?"
			 },
			 {
			 "text": "Did you recieve any error messages while configuring a Load Balancer? (If yes, please share the error message as well)"
			 }
		] }
 ] 
}
---
