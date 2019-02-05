{
	"resourceRequired": true,
	"title": "Issues Scaling a Database or Elastic Pool"
	"formElements": [{
			"id": "which_server",
			"order": 1,
			"controlType": "dropdownOptions",
			"displayLabel": "Please select which server contains the database you need assistance with.",
			"watermarktext": "Choose an option",
			"infoBalloonText": "This is a list of all of your associated servers.",
			"dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/servers?api-version=2015-05-01-preview",
				"jTokenPath": "serverList",
				"textProperty": "name",
				"valueProperty": "name",
				"textPropertyRegex": ".*"
			},
			"required": true,
			"useAsAdditionalDetails": false,
			"visibility": true
		}]
}
