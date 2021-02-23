<properties
  pagetitle="SSIS Crash or Unexpected Termination"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="hecepeda"
  selfhelptype="Generic"
  supporttopicids="32749435"
  resourcetags=""
  productpesids="14745"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  disableclouds=""
  articleid="sqlvm-ssis-crash-or-unexpected-termination"
  ownershipid="AzureData_AzureSQLVM" />

# Crash or Unexpected Termination

Resolve the following issues using the steps provided.

### **Issue: Package failures**
- Visual Studio SSDT crashes while opening/designing/building/executing a specific package
- Package execution fails with status **Unexpected Termination** for a package stored in SSISDB Catalog

## **Recommended Steps**

- Confirm if the project/package uses third-party tasks or components, or custom data flow/control flow tasks. If so, create a new SSIS Project, and then add the custom task to see if the task works as expected.

- If opening an existing project or adding an existing package with third-party components to a new project causes Visual Studio to crash, try opening another project or adding another package to an existing project that doesn't have the component to see if this project\package causes a crash. If the package opens successfully then the issue might be with the 3rd party component.

- The same holds for references to third-party DLLs in a Script task or component. If you're experiencing crashes with a package that contains a script task or component which references a third-party DLL, design a package that doesn't reference any third-party DLLs to confirm if that is the root of the issue.

### **Issue: Visual Studio SSDT crashes opening or designing packages that have Excel Source/Destination components**

## **Recommended Steps**

- Excel Connection Manager uses ACE OLEDB Driver to connect to Excel and the driver is shipped along with **Access Database Engine**. Check the version of **Access Database Engine** installed on the affected machine where Visual Studio SSDT is crashing.

- If you are using an Access Database Engine older than 2016, then upgrade to 2016 and confirm if the issue persists. If you are using Access Database Engine 2016 already, ensure that you are using the latest version of [Access Database Engine 2016](https://www.microsoft.com/download/details.aspx?id=54920).

- If the issue persists post installation of the latest version of Access Database Engine 2016, we suggest installing Access Database Engine 2010 and uninstalling Access Database Engine 2016 for a test.

Since Visual Studio is a 32-bit tool, install the 32-bit version of Access Database Engine to design packages.

- Access Database Engine 2016 installs two drivers on the machine:
  
   _ACE OLEDB 12.0_

   _ACE OLEDB 16.0_

  Access Database Engine 2010 installs one driver on the machine:

  _ACE OLEDB 12.0_

  Make sure that the connection string for Excel Connection uses ACE OLEDB 12.0 if Access Database Engine 2010 is being used.



If none of the above apply or help in resolving the issue, then we would be needed to collect crash dump at the time of the failure. Open a Microsoft support ticket so that an engineer can capture the required data/logs and troubleshoot the issue further.
