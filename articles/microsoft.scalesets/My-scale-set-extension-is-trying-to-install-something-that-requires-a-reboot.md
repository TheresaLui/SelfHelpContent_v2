<properties
    pageTitle="My scale set extension is trying to install something that requires a reboot"
    description="My scale set extension is trying to install something that requires a reboot"
    service="scalesets"
    author="negat"
    displayOrder="50"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# My scale set extension is trying to install something that requires a reboot, for instance: "commandToExecute": "powershell.exe -ExecutionPolicy Unrestricted Install-WindowsFeature –Name FS-Resource-Manager –IncludeManagementTools"

You could use the DSC extension. If the OS is 2012 R2, then Azure pulls in the WMF5.0 setup, reboots, and continues with the configuration. 