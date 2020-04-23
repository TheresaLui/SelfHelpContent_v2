<properties
	pageTitle="A user added an email application to their device, and then received an email stating that their device is not enrolled or not compliant."
	description="A user added an email application to their device, and then received an email stating that their device is not enrolled or not compliant."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="conditional_access_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="2ee4fe18-e50b-469e-a88c-4a5ec5fdad09"
	ownershipId="IntuneCxP_Intune"
/>

# A user added an email application to their device, and then received an email stating that their device is not enrolled or not compliant.

## **Recommended steps**

Users targeted with conditional access will receive a notification email if they do not meet your organization's access requirements. To resolve, we recommend one or more of the following solutions:

* If the device is presumed to be enrolled, advise the user to go to the Company Portal app and verify that it appears in the Company Portal. If it doesn't, the user should enroll the device. 
* In the Azure portal go to **Intune > Device compliance**. Under **Monitor** click **Device compliance**. View your device compliance report to verify that the user's device is marked as compliant.
* In the Azure portal go to **Intune > Device compliance**. Under **Manage**, click **Policies**. In the list of compliance policies, verify that a profile is assigned to your user's device. If no profile is assigned, then Intune will not be able to confirm the device's compliance status. 
* Edit the user's conditional access assignment.
    1.  In the Azure portal go to **Intune > Conditional access > Policies**.
    2.  Select a policy from the list. 
    3.  Click **Users and groups**.
    4.  To target a certain policy at someone, add them to the **Include** list. To ensure that a person is omitted from the policy, add them to the **Exclude** list.
