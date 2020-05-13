<properties
	pageTitle="Setup Conditional Access - Exchange on-premise Connector"
	description="Setup Conditional Access - Exchange on-premise Connector"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599633"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="df14f85b-1c75-4a55-9abf-45bf451443f3"
	ownershipId="IntuneCxP_Intune"
/>

# Setup Conditional Access - Exchange on-premises Connector

## **Recommended steps**

Review a couple solutions to potential issues with the Exchange Onpremise connector.

**The on-premises Exchange Connector installation keeps failing.**

* Ensure that all files in the on-premises Exchange Connector folder were not renamed or moved. Moving or renaming the folder's contents will cause the Exchange Connector installation to fail.

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

[Set up the Intune on-premises Exchange Connector in Microsoft Intune Azure](https://docs.microsoft.com/intune/exchange-connector-install)<br>
[What's conditional access?](https://docs.microsoft.com/intune/conditional-access)<br>
[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>


