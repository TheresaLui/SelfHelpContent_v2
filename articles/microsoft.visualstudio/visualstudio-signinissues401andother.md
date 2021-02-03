<properties
  pagetitle="Common causes of sign-in issues "
  service="microsoft.visualstudio"
  resource="account"
  ms.author="ccoop,cathmill"
  selfhelptype="Generic"
  supporttopicids="32572368,32572367"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopssigninissues401andother"
  ownershipid="Azure_DevOps_Services" />
# Common causes of sign-in issues 

## **Recommended Steps** 

### Troubleshooting Connectivity

1. Sign out of your browser. To do so, select the [Visual Studio sign out link](https://app.vssps.visualstudio.com/_signout) and let the sign-out process complete 
2. Delete the cookies in your browser. To delete cookies in most browsers, press Ctrl+Shift+Del 
3. Open Internet Explorer and delete the browser cookies. The Visual Studio IDE uses Internet Explorer cookies 
4. Close all browsers and close the Visual Studio IDE
5. Use a private browser session to retry the connection by directly going to the link dev.azure.com/<your organization name> 
6. If the issue is with the Visual Studio IDE, remove the connection and then add it again

## **Recommended Documents**

* [Resolve connection issues](https://docs.microsoft.com/azure/devops/user-guide/troubleshoot-connection?view=azure-devops)
* Want a quicker answer? Check out the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/) 
* To check the status of Azure DevOps Services or to review service-impacting issues, see [Azure DevOps Service Status](https://status.dev.azure.com/)
