<properties  
              pageTitle="Troubleshoot my VM firewall"
              description="Troubleshoot my VM firewall"
              service=""
              resource=""
              authors="manavis"
              displayOrder=""
              selfHelpType="generic"
              supportTopicIds="32615534"
              resourceTags=""
              productPesIds="14749"
              cloudEnvironments="public"
/>

# Troubleshoot my VM firewall

4 out of 5 customers resolved their connectivity issue using below steps:<br>

## **Recommended steps**

Use [serial console](data-blade:Microsoft_Azure_Compute.SerialConsoleBlade.resourceId.$resourceId) and open a CMD instance to query the current status

1. Query the firewall rules using any of the following methods:

	* Using the Display Name as a parameter:
	```   
	netsh advfirewall firewall show rule dir=in name=all | select-string -pattern "(DisplayName.*<FIREWALL RULE NAME>)" -context 9,4 | more
	```   
	* Using the Local Port the application is using:
	```   
	netsh advfirewall firewall show rule dir=in name=all | select-string -pattern "(LocalPort.*<APPLICAITON PORT>)" -context 9,4 | more
	```		
	* Using the Local IP the application is using:
	```
	netsh advfirewall firewall show rule dir=in name=all | select-string -pattern "(LocalIP.*<CUSTOM IP>)" -context 9,4 | more
	```   

2. If you see the rule disabled, then you can enable it as the following:
```
netsh advfirewall firewall set rule name="<RULE NAME>" new enable=yes
```   
3. For troubleshooting purposes in case you need to turn the firewall profiles OFF:
```
netsh advfirewall set allprofiles state off
```   
**Note:** Ensure you enable the firewall back after troubleshooting. A virtual machine reboot is not necessary for this change to kick in.
