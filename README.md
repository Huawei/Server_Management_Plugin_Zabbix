****************************************************************************
Zabbix Plugin Pack for Huawei Device
****************************************************************************

I. General Information

    Name:     Zabbix Plugin Packsage for Huawei Server
    Function: Query, Monitoring
    Version:  1.2

	
II. Description

    Integrated in the Zabbix software, Huawei Zabbix plug-in is provided as a Zabbix template. Users can directly use it or use it for secondary development. The Zabbix plug-in can be used to monitor the iBMC, HMM, CCU component, EMM, or SWI.

	
III. Compatibility Information


<table>
   <tr>
      <td>Managed  Object</td>
      <td>Compatible  Zabbix Version</td>
      <td><span style="white-space:nowrap;">Version  Dependency&emsp;&emsp;&emsp;&emsp;</span></td>
      <td><span style="white-space:nowrap;">Hardware  Compatibility&emsp;&emsp;&emsp;</span></td>
      <td><span style="white-space:nowrap;">Interface  Protocol&emsp;&emsp;&emsp;&emsp;</span></td>
   </tr>
   <tr>
      <td>HMM</td>
      <td>Zabbix 3.4, Zabbix 4.0</td>
      <td>HMM V686D or later</td>
      <td>Blade server: E9000</td>
      <td>SNMP v2c</td>
   </tr>
   <tr>
      <td>iBMC</td>
      <td>Zabbix3.4, Zabbix 4.0, Zabbix 5.0</td>
      <td>iBMC V294 or later</td>
      <td>Rack server: RH1288 V3, RH2288 V3, RH2288H V3, RH5885 V3, RH8100 V3, 1288H V5, 2288H V5, 2488 V5, 2288 V5, 2288X V5; 
	      High-density server: XH321 V3, XH620 V3, XH622 V3, XH628 V3; 
	      Heterogeneous server: G560 V5; 
	      Blade server: CH121L V5</td>
      <td>SNMP v2c</td>
   </tr>
   <tr>
      <td>CCU</td>
      <td> Zabbix 3.4, Zabbix 4.0, Zabbix 4.4</td>
      <td>CCU V156RC or later</td>
      <td>-</td>
      <td>SNMP v3</td>
   </tr>
   <tr>
      <td>EMM</td>
      <td>Zabbix 3.4, Zabbix 4.2</td>
      <td>iBMC V380 or later</td>
      <td>Management module: MM921</td>
      <td> SNMP trap v2c, SNMP trap v3</td>
   </tr>
   <tr>
      <td>SWI</td>
      <td> Zabbix 3.4, Zabbix 4.2</td>
      <td>iBMC V396 or later</td>
      <td>Switch module: CX320, CX621</td>
      <td>SNMP trap v2c,  SNMP trap v3</td>
   </tr>
</table>


	
VI. Additional Resources

    For more information consult User Guide. https://github.com/Huawei/Server_Management_Plugin_Zabbix/tree/master/docs
