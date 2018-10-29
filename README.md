# 1.Zabbix Template Introduction

Zabbix is free and open-source software. After a Huawei iBMC or HMM template is imported and community names of servers are configured in the template, you can view server asset information, monitor server component alarms, and view server temperature change curves, CPU and memory usage change curves, and real-time power change diagrams on the Zabbix WebUI.

**Zabbix Template Names:**
-	Huawei - ValueMap V1.0.xml
-	Huawei - iBMC V1.0.xml
-	Huawei - HMM V1.0.xml

**Supported Versions:**
-	Zabbix 3.4.X
-	Zabbix 4.0.X

**Mapping Software:**
-	MM910: (U54) 6.86D or later
-	iBMC: 2.94 (U25) or later


# 2.Template Functions

**iBMC Template:**
-	Latest data: CPU, fan, hard disk, iBMC system information, memory, power supply, RAID controller card, and temperature
-	Problems and triggers: system health status, CPU status, fan status, power supply status, hard disk status, and memory status
-	Graphs: inlet temperature, power consumption, system CPU usage, averagePower, peakPower, presentSystemPower and system memory usage
-	Inventory: type, name, OS, serial number, tag, and MAC address

**HMM Template:**
-	Latest data: CPU, fan, power supply, switch, system information, and temperature
-	Problems and triggers: system health, chassis health, SMM health, blade status, fan status, power supply status, and switch status
-	Graphs: ambient temperature, inlet temperature, LSW temperature, outlet temperature, real-time chassis power, blade CPU power, blade inlet temperature, real-time blade power, and blade system CPU usage
-	Inventory: type, name, OS, serial number, tag, and MAC address


# 3.Template Configuration

## 3.1 Configuring the iBMC
- Step 1	Log in to the iBMC WebUI.
- Step 2	Choose Configuration > System.
- Step 3	Select SNMPv2c, and set the community name.

## 3.2 Configuring the HMM
- Step 1	Log in to the HMM CLI.
- Step 2	Run the following command to configure the SNMPv2c protocol:
		smmset -l smm -d snmpconfig -v v2c enable 
- Step 3	Enter y to confirm the configuration information.
- Step 4	Run the following command to enter the community name configuration:
		smmset -l smm -d snmpconfig -v community 
- Step 5	Enter a community name.

## 3.3 Importing and Configuring a Template
**3.3.1 Importing a ValueMap Template**
- Step 1	Log in to GitHub and obtain the Huawei Server ValueMap V1.1.xml template.
- Step 2	Log in to the Zabbix WebUI.
- Step 3	Choose Administration > General.
- Step 4	Select Value mapping from the drop-down list box.
- Step 5	Click Import to go to the import page.
- Step 6	Click Browse and select the template obtained in step 1.
- Step 7	Click Import.

**3.3.2 Importing an iBMC or HMM Template**
- Step 1	Log in to GitHub and obtain the Huawei Server iBMC Template V1.1.xml or Huawei Server HMM Template V1.1.xml template.
- Step 2	Log in to the Zabbix WebUI.
- Step 3	Choose Configuration > Templates.
- Step 4	Click Import to go to the import page.
- Step 5	Click Browse and select the template obtained in step 1.
- Step 6	Click Import.

**3.3.3 Configuring a Template**
- Step 1	Log in to the Zabbix WebUI.
- Step 2	Choose Configuration > Templates.
- Step 3	Select the template to be imported.  
- Step 4	Select Macros and set {$SNMP_COMMUNITY} and {$SNMP_PORT}.  
	The value of {$SNMP_COMMUNITY} is the community name configured in section 3.1 or section 3.2.   
	Retain the default value 161 for {$SNMP_PORT}.   
- Step 5	Click Update.

**3.3.4 Adding a Host**
- Step 1	Log in to the Zabbix WebUI.
- Step 2	Choose Configuration > Hosts.The Hosts page is displayed.
- Step 3	Select Create Hosts to go to the creation page.  
	Set In groups under Groups to Huawei Server.  
	Set IP address and Port under SNMP interfaces to the iBMC IP address and 161 respectively.  
- Step 4	Click Update.

# 4.Zabbix share

- Huawei Server iBMC Template: https://share.zabbix.com/cat-server-hardware/huawei/huawei-server-ibmc-template
- Huawei Server HMM Template:  https://share.zabbix.com/cat-server-hardware/huawei/huawei-server-hmm-template
