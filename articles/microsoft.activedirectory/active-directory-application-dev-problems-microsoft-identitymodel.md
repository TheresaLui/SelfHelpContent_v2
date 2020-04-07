<properties
    pageTitle="I have problems using using Microsoft.IdentityModel (ASP.NET Core and ASP.NET)"
    description="I have problems using using Microsoft.IdentityModel (ASP.NET Core and ASP.NET)"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jmprieur"
    ms.author="jmprieur"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32596874"
    resourceTags=""
    productPesIds="16575"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="cb6ca4c1-d40b-44fc-bfd9-46dea8773765"
	ownershipId="AzureIdentity_AppDevelopmentAndRegistration"
/>

# I have problems using Microsoft.IdentityModel (ASP.NET Core and ASP.NET)

## **Recommended Steps**

### **How can I enable debugging in my ASP.NET or ASP.NET Core Web app or Web API?**

To debug ASP.NET Core apps, you need to enable the [developer exception page](https://docs.microsoft.com/aspnet/core/fundamentals/error-handling#developer-exception-page), and also review [error handling in ASP.NET Core](https://docs.microsoft.com/aspnet/core/fundamentals/error-handling)
See also:

* [Use multiple environments in ASP.NET Core](https://docs.microsoft.com/aspnet/core/fundamentals/environments)
* [Debug ASP.NET or ASP.NET Core apps in Visual Studio](https://docs.microsoft.com/visualstudio/debugger/how-to-enable-debugging-for-aspnet-applications?view=vs-2019)

### **How can I enable PII in my ASP.NET Core Web app / API?**

By default, we do not include any potential PII (personally identifiable information) in the Microsoft.IdentityModel exceptions, in order to be compliant with GDPR.
In order to see all the information provided in the exceptions, you will need to set `IdentityModelEventSource.ShowPII` to `true`.

### **How do I debug the middleware events in my ASP.NET Core Web app / API?**

You can debug middleware events in:
- Web apps, by subscribing to the OpenID Connect middleware events. See example code on how to do that in: [OpenIdConnectMiddlewareDiagnostics](https://github.com/Azure-Samples/active-directory-aspnetcore-webapp-openidconnect-v2/blob/db7f74fd7e65bab9d21092ac1b98a00803e5ceb2/Microsoft.Identity.Web/Resource/OpenIdConnectMiddlewareDiagnostics.cs)
- Web APIs, by subscribing to the OpenID Connect middleware events. See example code on how to do that in: [JwtBearerMiddlewareDiagnostics](https://github.com/Azure-Samples/active-directory-aspnetcore-webapp-openidconnect-v2/blob/db7f74fd7e65bab9d21092ac1b98a00803e5ceb2/Microsoft.Identity.Web/Resource/JwtBearerMiddlewareDiagnostics.cs)

## **Recommended Documents**

The following article describes the scenarios involving Microsoft.IdentityModel including Web apps and Web APIs, written in ASP.NET Core and ASP.NET:

* [Web app that signs in users](https://docs.microsoft.com/azure/active-directory/develop/scenario-web-app-sign-user-overview?tabs=aspnetcore)
* [Web app that calls web APIs](https://docs.microsoft.com/azure/active-directory/develop/scenario-web-app-call-api-overview)
* [Protected web API](https://docs.microsoft.com/azure/active-directory/develop/scenario-protected-web-api-overview)
* [Web API that calls web APIs](https://docs.microsoft.com/azure/active-directory/develop/scenario-web-api-call-api-overview)
* [IdentityModel extensions for .Net](https://github.com/AzureAD/azure-activedirectory-identitymodel-extensions-for-dotnet/wiki)
