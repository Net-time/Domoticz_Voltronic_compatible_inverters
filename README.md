# Domoticz_Voltronic_compatible_inverters
Python plugin for inverters that use AXPERT KS&amp;MKS&amp;V Communication Protocol.
If your inverter have a setting for Modbus address or use modbus with fixed adress this is not for you.

Connects to rs232 port interface on inverter via USB serial adapter.
Option to enable SNMP for automated shutdowns on grid fail.

Devices for the most usable inverter parameters in QPIGS reply.
IDX unit 31-32 have calculated values and may differ slightly from display on inverter.

# Todo:
finish readme.
Implement SMNP server as thread in Domoticz.
First upload.
Make plugin check if device deleted.

# SNMP:
Original SNMP code from https://github.com/delimitry/snmp-server.
The scripts does not read manufacturer/model, as this is only to speed up a NAS or similar to connect to Pro inverters.
Enter manually or leave default  as is, do not enter a Pro inverter.
But it will speed up the process anyway as the NAS will identify it as a "noBrand" and skip to standard RFC 1628 requests.
Inverter status is taken from main grid voltage "Online/OnBattery", as I only use QPIGS to get inverter data.
Battery charge percentage is read but battery time remaining will be a hack.
Tested with Synology NAS, and my plan is to also use it to safeley shut down my Raspberry Pi's.



<img width="1530" height="705" alt="image" src="https://github.com/user-attachments/assets/a287c3a6-2b93-4beb-bcc9-8f966f3ab148" />

Both below connections occur within the same Brand, (Vevor in my case).
<img width="962" height="422" alt="image" src="https://github.com/user-attachments/assets/c1803460-6f20-434d-97ac-45de353eb6c2" />
