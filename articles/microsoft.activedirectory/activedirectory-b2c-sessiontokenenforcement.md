 <properties
	pageTitle="Business to Consumer (B2C)/Session token configuration not being enforced"
	description="Business to Consumer (B2C)/Session token configuration not being enforced"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="parakhj"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Session token configuration is not being enforced

If you use the "Sign-in" policy, your custom session token duration will not be enforced. The workaround is to use a combined "Sign in / Sign up" policy instead. This issue originates from the fact that the "Sign-up or Sign-in" policy leverages a newer and improved policy implementation compared to the older "Sign-in" policy.