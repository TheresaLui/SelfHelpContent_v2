<properties
	pageTitle="Configure Load Distribution"
	description="Configure Load Distribution"
	authors="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588973"
	productPesIds="16098"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId=""
/>
# SLB - Configure Load Distribution
---
{
 "resourceRequired": true,
 "title": "Configure Load Distribution",
 "fileAttachmentHint": "",
 "formElements": [	 
	 {
	 "id": "config_lb_nva"
	 "order": 1,
	 "controlType": "dropdown",
	 "displayLabel": "Is there a third party virtual appliance in the data-path?",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Yes",
		 "text": "Yes"
		 },
		 {
		 "value": "No",
		 "text": "No"
		 },
	 ],
	 "required": true
	 },
	 {
	 "id": "config_lb_nated"
	 "order": 2,
	 "controlType": "dropdown",
	 "displayLabel": "Are the packet reaching Load Balancer NAT'd to specific destination(s)?",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Yes",
		 "text": "Yes"
		 },
		 {
		 "value": "No",
		 "text": "No"
		 },
	 ],
	 "required": true
	 },
	 {
	 "id": "config_lb_cloudsvc"
	 "order": 3,
	 "controlType": "dropdown",
	 "displayLabel": "Are you trying to configure load distribution mode for Cloud Services?",
	 "watermarkText": "Choose an option",
	 "dropdownOptions": [
		 {
		 "value": "Yes",
		 "text": "Yes"
		 },
		 {
		 "value": "No",
		 "text": "No"
		 },
	 ],
	 "required": true
	 },		 
	 {
		 "id": "problem_start_time",
		 "order": 4,
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
