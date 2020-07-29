<properties
  pagetitle="Windows Virtual Desktop - Issues configuring tenant using PowerShell"
  service=""
  resource=""
  ms.author="evas"
  selfhelptype="Generic"
  supporttopicids="32727875"
  resourcetags=""
  productpesids="16582"
  cloudenvironments="public"
  articleid="816619f7-c15e-4d55-b984-5804ccbedf5e"
  ownershipid="Windows_Virtual_Desktop" />
# Windows Virtual Desktop - Issues configuring tenant using PowerShell

## **Recommended Steps**
Configuring your service environment using Windows Virtual Desktop with Azure Resource Manager integration:

* [Review steps creating a host pool with PowerShell](https://docs.microsoft.com/azure/virtual-desktop/create-host-pools-powershell)
* [Review PSCmdlet examples to add a Workspace](https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdworkspace?view=azps-4.3.0)

When using Windows Virtual Desktop (classic):

* Are you logged on with the service?

   * Use Add-RdsAccount -DeploymentUrl https://rdbroker.wvd.microsoft.com
   * Next authenticate when prompted

* Troubleshoot 
   * [User not authorized querying the service](https://docs.microsoft.com/azure/virtual-desktop/virtual-desktop-fall-2019/troubleshoot-set-up-issues-2019#error-the-user-isnt-authorized-to-query-the-management-service)
   * [Tenant and host pool creation](https://docs.microsoft.com/azure/virtual-desktop/virtual-desktop-fall-2019/troubleshoot-set-up-issues-2019)
   
## **Recommended Documents**

* [Get started with Windows](https://docs.microsoft.com/azure/virtual-desktop/)

Windows Virtual Desktop with Azure Resource Manager integration:

* [PowerShell Troubleshooting](https://docs.microsoft.com/azure/virtual-desktop/troubleshoot-powershell)
* [PowerShell reference guide](https://docs.microsoft.com/powershell/module/az.desktopvirtualization/?view=azps-4.3.0&viewFallbackFrom=azps-4.2.0#desktopvirtualization)

Windows Virtual Desktop (classic):

* [Create Service Principal and Role Assignment](https://docs.microsoft.com/azure/virtual-desktop/virtual-desktop-fall-2019/create-service-principal-role-powershell)
* [PowerShell reference guide](https://docs.microsoft.com/powershell/windows-virtual-desktop/overview)
