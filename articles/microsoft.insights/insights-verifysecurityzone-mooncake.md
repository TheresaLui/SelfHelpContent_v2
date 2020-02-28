<properties 
	pageTitle="I need to verify my security zone"
	description="I need to verify my security zone"
	service="microsoft.insights"
	resource="components"
	authors="chlon"
	ms.author="chlon"
	displayOrder="14"
	selfHelpType="resource"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="insights-verifysecurityzone-mooncake"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# I need to verify my security zone

## **Recommended Steps**

An authentication related error occurred (during authentication or during access token generation). The portal may have no way to recover without changing browser settings.

1. Verify third party cookies are enabled in the browser
2. Did you use a favorite, bookmark, or saved link to open the Analytics portal? Are you signed in with different credentials than you used when you saved the link?
3. Try using an in-private/incognito browser window (after closing all such windows). You'll have to provide your credentials.
4. Open another (ordinary) browser window and go to Azure. Sign out. Then open your link and sign in with the correct credentials.
5. Edge and Internet Explorer users can also get this error when trusted zone settings are not supported. Verify both Analytics portal and Azure Active Directory portal are in the same security zone.

## **Recommended Documents**

* [Detailed security zone verification steps](https://docs.azure.cn/azure-monitor/azure-monitor-app-hub#authentication)
