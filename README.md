# Domoticz_Voltronic_compatible_inverters
Python plugin for inverters that use AXPERT KS&amp;MKS&amp;V Communication Protocol 

Connects to rs232 port interface on inverter via USB serial adapter.
Option to enable SNMP for automated shutdowns on grid fail.

Devices for the most usable inverter parameters.
IDX unit 31-32 have calculated values and may differ slightly from display on inverter.

Todo:
finish readme.
Implement SMNP server as thread in Domoticz.
First upload.
Cable pinouts.

SNMP:
Original SNMP code from https://github.com/delimitry/snmp-server.
The script does not read manufacturer/model, as this is only to speed up a NAS or similar to connect to Pro inverters.
But it will speed up the process anyway as the NAS will identify it as a "noBrand" and skip to standard requests.
Inverter status is taken from main grid voltage "Online/OnBattery".
Battery charge is read but battery time remaining will be a hack.



<img width="1530" height="705" alt="image" src="https://github.com/user-attachments/assets/a287c3a6-2b93-4beb-bcc9-8f966f3ab148" />
