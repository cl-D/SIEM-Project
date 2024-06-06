# Cybersecurity SIEM Honeypot Project

## Introduction
The idea behind this project is to create a VM in Microsoft Azure that serves as a honeypot for attackers. This VM is running Windows 10 Pro with all of its ports open and Windows Defender Firewall turned off. As threat actors try to brute force their way into the VM through RDP atacks, the Windows Event Viewer logs for failed login attempts are parsed for the attacker's geographic information. Using the [ipgeolocation.io](https://app.ipgeolocation.io/) API, the attacker's IP is mapped to a general location on the map (city, country) and this data is then uploaded to a table in Microsoft's Log analytics workspace. Lastly, the data is queried in a workbook in Microsoft Sentinel and graphed on a map.
