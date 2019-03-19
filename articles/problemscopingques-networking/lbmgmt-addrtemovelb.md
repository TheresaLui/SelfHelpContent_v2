{
 "resourceRequired": true,
 "title": "Add or Remove Load Balancer resources",
 "fileAttachmentHint": "",
 "formElements": [	 
	 {
		 "id": "problem_start_time",
		 "order": 2,
		 "controlType": "datetimepicker",
		 "displayLabel": "When did the problem begin?",
		 "required": true
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
			 "text": "Do you need help with any specific management problem?"
			 },
			 {
			 "text": "Did you recieve any error messages while making changes to the Load Balancer configuration? (If yes, please share the error message as well)"
			 }
		] }
 ] }