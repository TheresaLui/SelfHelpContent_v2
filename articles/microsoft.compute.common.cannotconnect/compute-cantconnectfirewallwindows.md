<properties  
    pageTitle="Troubleshoot my VM firewall"
    description="Troubleshoot my VM firewall"
    service=""
    resource=""
    authors="scottAzure,timbasham"
    ms.author="scotro,tibasham"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615534,32639648"
    resourceTags=""
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="72a1d281-9123-421c-9cf6-90fed2618648"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshoot my VM firewall

4 out of 5 customers resolved their VM firewall issue using the steps below.<br>

## **Recommended Steps**

Use [Serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) and open a CMD instance to query the current status.<br>

1. Query the firewall rules using any of the following methods:

    * Using the Display Name as a parameter:<br>

        ```
        netsh advfirewall firewall show rule dir=in name=all | select-string -pattern "(DisplayName.*<FIREWALL RULE NAME>)" -context 9,4 | more
        ```

    * Using the Local Port the application is using:<br>

        ```
        netsh advfirewall firewall show rule dir=in name=all | select-string -pattern "(LocalPort.*<APPLICAITON PORT>)" -context 9,4 | more
        ```

    * Using the Local IP the application is using:<br>

        ```
        netsh advfirewall firewall show rule dir=in name=all | select-string -pattern "(LocalIP.*<CUSTOM IP>)" -context 9,4 | more
        ```

2. If you see the rule disabled, then you can enable it as the following:

    ```
    netsh advfirewall firewall set rule name="<RULE NAME>" new enable=yes
    ```

3. For troubleshooting purposes in case, you need to turn the firewall profiles OFF:

    ```
    netsh advfirewall set allprofiles state off
    ```

**Note:** Ensure you re-enable the firewall after troubleshooting. A virtual machine reboot is not necessary for this change to take effect.<br>

## **Recommended Documents**

* [Guest OS firewall is blocking all inbound traffic](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/guest-os-firewall-blocking-inbound-traffic)<br>
* [Guest OS firewall is misconfigured](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/guest-os-firewall-misconfigured)<br>
* [How to disable the guest OS firewall](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/disable-guest-os-firewall-windows)<br>
* [Enable or disable a guest OS firewall rule](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/enable-disable-firewall-rule-guest-os)<br>
* [Troubleshooting Windows Firewall with Advanced Security in Windows Server 2012](https://social.technet.microsoft.com/wiki/contents/articles/13894.troubleshooting-windows-firewall-with-advanced-security-in-windows-server-2012.aspx)<br>
* [Learn more about Serial Console](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-windows)
