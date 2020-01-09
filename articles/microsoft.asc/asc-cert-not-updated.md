<properties
	pageTitle="ASC/SSL Certificate not updated after renew or rekey"
	description="ASC/SSL Certificate not updated after renew or rekey"
	service="microsoft.asc"
	resource="asc"
	authors="cts-shrahman, cts-shrahman"
    ms.author="shrahman,curibe"
	displayOrder="4"
	selfHelpType="generic"
	supportTopicIds="32693164"
	resourceTags=""
	productPesIds="16512"
	cloudEnvironments="public"
	articleId="578ffdca-6a2e-464e-85f0-fa70a6c34106"
/>

# ASC/Renewing-Rekeying

## **Recommended steps**

After renewing or rekeying an App Service certificate, there will be a sync operation which will automatically update the hostname bindings for the certificate in App Service without causing any downtime to your apps within 48 hours
