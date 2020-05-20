<properties
	pageTitle="Setup Conditional Access - Setup App Based Conditional Access"
	description="Setup Conditional Access - Setup App Based Conditional Access"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599675"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8a6f05d4-078d-4f93-8e47-9c5880f07db8"
	ownershipId="IntuneCxP_Intune"
/>

# Setup Conditional Access - Setup App Based Conditional Access

## **Recommended steps**

**A user added an email application to their device, and then received an email stating that their device is not enrolled or not compliant.**

Users targeted with conditional access will receive a notification email if they do not meet your organization's access requirements. To resolve, we recommend one or more of the following solutions:

* If the device is presumed to be enrolled, advise the user to go to the Company Portal app and verify that it appears in the Company Portal. If it doesn't, the user should enroll the device. 
* In the Azure portal go to **Intune > Device compliance**. Under **Monitor** click **Device compliance**. View your device compliance report to verify that the user's device is marked as compliant.
* In the Azure portal go to **Intune > Device compliance**. Under **Manage**, click **Policies**. In the list of compliance policies, verify that a profile is assigned to your user's device. If no profile is assigned, then Intune will not be able to confirm the device's compliance status. 
* Edit the user's conditional access assignment.
    1.  In the Azure portal go to **Intune > Conditional access > Policies**.
    2.  Select a policy from the list. 
    3.  Click **Users and groups**.
    4.  To target a certain policy at someone, add them to the **Include** list. To ensure that a person is omitted from the policy, add them to the **Exclude** list.

## **Recommended documents**

[How to configure Exchange Online conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-mam#exchange-online-policy)<br>
[App-based conditional access with Intune](https://docs.microsoft.com/intune/app-based-conditional-access-intune-create)<br>
[What's conditional access?](https://docs.microsoft.com/intune/conditional-access)<br>
[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>