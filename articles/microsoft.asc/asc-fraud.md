<properties
	pageTitle="ASC/Pending Verification due to Fraud Protection"
	description="ASC/Pending Verification due to Fraud Protection"
	service="microsoft.asc"
	resource="asc"
	ms.author="shrahman"
	authors="cts-shrahman"
	displayOrder="6"
	selfHelpType="generic"
	supportTopicIds="32604396"
	resourceTags=""
	productPesIds="16512"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="fdccae2e-f103-4a82-be97-33f6cc3a7658"
	ownershipId="Compute_AppService"
/>

# ASC/Pending Verification due to Fraud Protection

## **Recommended Steps**

When an App Service Certificate was marked as fraud, you will see the error "Your certificate has been flagged for possible fraud. The request is currently under review." If the certificate is marked as Fraud and has not been resolved after 24 hours, then follow the steps below:

1. Go to App Service certificate in Azure portal
2. Click on Certificate Configuration -> Step 2 : Verify -> Domain Verification
3. Click on Email Instructions which will send an email to GoDaddy to resolve the issue

## **Recommended Documents**

* [My App Service certificate is flagged for fraud. How do I resolve this?](https://azure.github.io/AppService/2017/07/24/FAQ-SSL-certificates-for-Web-Apps-and-App-Service-Certificates#my-app-service-certificate-is-flagged-for-fraud-how-do-i-resolve-this) 
