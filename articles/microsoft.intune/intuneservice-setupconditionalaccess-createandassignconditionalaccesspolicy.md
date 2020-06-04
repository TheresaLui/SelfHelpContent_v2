<properties
	pageTitle="Setup Conditional Access - Create and assign conditional access policy"
	description="Setup Conditional Access - Create and assign conditional access policy"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599623"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="4fa19219-ec91-4595-9ad3-41b3ac33d2a0"
	ownershipId="IntuneCxP_Intune"
/>

# Setup Conditional Access - Create and assign conditional access policy

## **Recommended steps**

Review the below solutions to common issues with conditional access:

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

**I tried to create a conditional access policy that blocks all mail apps on my organization's Windows computers. Currently, however, only native mail apps are being blocked.**

On a Windows computer, conditional access only applies to:

  * The native mail app 
  * Microsoft Office 2016
  * Microsoft Office 2013 when modern authentication is enabled

To block Microsoft Office 2013 when modern authentication is disabled, an earlier version of Office, or to block all mail apps, you must:

  * Register the device in Azure Active Directory.
  * Configure Azure Active Directory Federation Services (ADFS). To learn how to configure ADFS, see [Set up SharePoint Online and Exchange Online for Azure Active Directory conditional access.](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-no-modern-authentication)

## **Recommended documents**

[How to create and assign a conditional access policy for Exchange on-premises and legacy Exchange Online Dedicated in Microsoft Intune](https://docs.microsoft.com/intune/conditional-access-exchange-create)<br>
[What's conditional access?](https://docs.microsoft.com/intune/conditional-access)<br>
[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>