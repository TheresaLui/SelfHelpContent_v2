<properties
    pageTitle="How to set server timezone"
    description="How do I set the server Timezone for my web app?"
    service="microsoft.web"
    resource="sites"
    authors="aashu"
    selfHelpType="faq"
    keywords="Timezone, server time"
    resourceTags="windows, linux"   
    productPesIds="14748"
/>

# How do I set the server Timezone for my web app

* In the Azure Portal, open the<!--data-blade:WebsitesExtension.WebsiteConfigSiteSettings --> Application settings <!--/data-blade-->menu of your Azure App Service.
* In the 'Application Settings' menu, scroll down to find 'App settings' and add a setting as shown below
    * Key = WEBSITE_TIME_ZONE
    * Value = Desired Time Zone
* Save changes
