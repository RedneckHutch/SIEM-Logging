# Still in-progress
- [x] SIEM-Logging
- [ ] Window-Event-Collector
- [ ] Syslog Server
- [ ] Window-Event-Logging
- [ ] Powershell-Logging
- [ ] DNS-Logging
- [ ] DHCP-Logging
- [ ] SYSMON-Logging
- [ ] SPAN Port Configuration
- [ ] Resources
# SIEM-Logging
SIEMs are great if you have the configured correctly. They are still only as good as the data that you are putting into them. There are two things that you will typically see within an organization and they either log everything or hardly log anything within their SIEM. They may log everything because it is easy. They do not want to miss a critical log but there is a point when to much data is a bad thing. To much data can increase cost, slow down search times, and making it more difficult to locate useful data within the logs. This can unlimately cause fatigue on employees attempting to parse through the overwhelming amounts of data. While other organizations may not have the budget to increase their SIEM ingestion. The goal of this repository is to get you and your team on the right track.  <br />

Logging ultimately comes down to your organization and the use cases that will be implemented into your SIEM. Wether you a required for compliance reason, audit, or strictly security reasons. We will focus on forming a great baseline which you can later modify to fit your exact needs. It is highly recommended to following a framework such as [NIST](https://www.nist.gov/) Or even [Mitre Att&CK](https://attack.mitre.org/). <br />

It is highly recommended to have a well rounded knowledge of GPO. <- Inprogress

- [Window Event Collector](#Window-Event-Collector)
- [Window Event Logging](#Window-Event-Logging)
- [SYSMON-Logging](#SYSMON)
- [DNS Logging](#DNS-Logging)

## Window-Event-Collector
Window Event Collectors, also known as WEC allow administrators to get events from remote computers and store them in a local event log on the collector computer. The data that has been forwarded to the collector is saved on the collector as if they were on the orignating host. But additional information is added regarding event forwarding. It is possible to manually configure each remote computer to send logs to the WEC. But group policies are typically used to configure the remote computers to forward events to the WEC.<br /><br />

Why should you use a window event collector? Has your organization ever been tasked with gathering window events from several endpoints? Or perhaps you are performing an incident response investigation and need to ingest all the logs to a centralized location? While using agents such as FileBeat or Splunk Universal Forwarders is still highly recommended, but perhaps you are not able to install those agents on every endpoint. Well this is where the WEC shines! As more and more agents are installed on endpoints you start running into a multitude of issues such as performance issues, agents just not functioning correctly, or even management approval to do so. <br />

https://learn.microsoft.com/en-us/windows/win32/wec/windows-event-collector

## Window-Event-Logging
Window event logging can get over looked very easly. It also can seem like a daughting task for some. Instead of recreating the wheel. I would highly recommend reviewing [The Windows Logging Cheat Sheets](https://www.malwarearchaeology.com/cheat-sheets) by [MalwareArchaeology](https://www.malwarearchaeology.com).<br />

List out the System audit policy: AuditPol /get /category:* <br /><br />
To set an item: Auditpol /set /category:"Account Management" /success:enable /failure:enable<br /><br />
To set a subcategory individually: Auditpol /set /subcategory:"Directory Service Access" /success:disable /failure:disable<br />





<table>
    <tr>
        <td>
            <a href="https://static1.squarespace.com/static/552092d5e4b0661088167e5c/t/5c586681f4e1fced3ce1308b/1549297281905/Windows+Logging+Cheat+Sheet_ver_Feb_2019.pdf" target="_blank">WINDOWS LOGGING CHEAT SHEET</a>
        </td>
        <td>
            This “Windows Logging Cheat Sheet” is intended to help you get started setting
up basic and necessary Windows Audit Policy and Logging. By no means is this list
extensive; but it does include some very common items that should be enabled,
configured, gathered and harvested for any Log Management Program. Start with
these settings and add to it as you understand better what is in your logs and
what you need. Resource from (www.malwarearchaeology.com)
        </td>
    </tr>
</table>


## Powershell-Logging
<table>
    <tr>
        <td>
            <a href="https://www.mandiant.com/resources/blog/greater-visibility" target="_blank">Greater Visibility Through PowerShell Logging</a>
        </td>
        <td>
            Mandiant is continuously investigating attacks that leverage PowerShell throughout all phases of the attack. A common issue we experience is a lack of available logging that adequately shows what actions the attacker performed using PowerShell. In those investigations, Mandiant routinely offers guidance on increasing PowerShell logging to provide investigators a detection mechanism for malicious activity and a historical record of how PowerShell was used on systems.
        </td>
    </tr>
</table>


## SYSMON-Logging
## DNS-Logging
## Resources
<table>
    <tr>
        <td>
            <a href="https://github.com/olafhartong/sysmon-modular" target="_blank">Sysmon-modular</a>
        </td>
        <td>
            Description pending
        </td>
    </tr>
        <tr>
        <td>
            <a href="https://learn.microsoft.com/en-us/windows/win32/wec/windows-event-collector" target="_blank">Window Event Collector</a>
        </td>
        <td>
            Reference to Microsoft's documentation regarding window event collectors.
        </td>
    </tr>
</table>
