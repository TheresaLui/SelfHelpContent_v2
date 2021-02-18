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

###  **Visual Studio SSDT is crashing while opening\designing\building\executing a specific package**

or

### **Package execution fails with status 'Unexpected Termination' for a package stored in SSISDB Catalog.**

## **Recommended Steps**

- Please confirm if the Project\Package uses any 3rd party tasks\components or custom data flow\control flow tasks.

- If there are any custom tasks\components or 3rd party tasks\components, try to create a new SSIS Project and add the custom task to see if the task is working as expected or not.

- If opening an existing project or adding an existing package with 3rd party components to a new project causes Visual Studio to crash, try opening another Project or adding another package to an existing Project which does not have the 3rd party\custom component to see if this project\package causes a crash.

If the package opens successfully then the issue might be with the 3rd party component.

- The same holds for references to 3rd party DLLs in a Script task\component. If packages with script task\component which reference a 3rd party DLL are causing a crash, please design a package which does not reference any 3rd party DLLs to confirm if that is the root of the issue.

### **Visual Studio SSDT is crashing while opening\designing only those packages which have Excel Source\Destination components.**

## **Recommended Steps**

- Excel Connection Manager uses ACE OLEDB Driver to connect to Excel and the driver is shipped along with **Access Database Engine**. Check the version of **Access Database Engine** installed on the affected machine where Visual Studio SSDT is crashing.


- If you are using an **Access Database Engine** lower than **2016**, then please **upgrade to 2016** and confirm if the issue persists. If you are using Access Database Engine 2016 already then please ensure that you are using the latest version of [Access Database Engine 2016](https://www.microsoft.com/download/details.aspx?id=54920)

- If the issue persists post installation of the latest version of Access Database Engine 2016, we suggest installing **Access Database Engine 2010** and **uninstalling Access Database Engine 2016 for a test**.

Since Visual Studio is a 32-bit tool, **32-bit version** of Access Database Engine will be needed to be installed to design packages.

- Access Database Engine 2016 installs two drivers on the machine:
  
  _ACE OLEDB 12.0_

  _ACE OLEDB 16.0_

  Access Database Engine 2010 installs one driver on the machine:

  _ACE OLEDB 12.0_

   Please make sure that the connection string for Excel Connection uses ACE **OLEDB 12.0** if **Access Database Engine 2010** is being used.



If none of the above apply or help in resolving the issue, then we would be needed to collect crash dump at the time of the failure. Please open a Microsoft support ticket so that an engineer can capture the required data\logs and troubleshoot the issue further.
