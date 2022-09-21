# SIEM-Logging

- [Window Event Collector](#Window-Event-Collector)
- [Window Event Logging](#Window-Event-Logging)
- [SYSMON-Logging](#SYSMON)
- [DNS Logging](#DNS-Logging)

## Window-Event-Collector
Window Event Collectors, also known as WEC allow administrators to get events from remote computers and store them in a local event log on the collector computer. The data that has been forwarded to the collector is saved on the collector as if they were on the orignating host. But additional information is added regarding event forwarding. It is possible to manually configure each remote computer to send logs to the WEC. But group policies are typically used to configure the remote computers to forward events to the WEC..<br /><br />

Why should you use a window event collector? Has your organization ever tasked with gathering window event logs from a large number of endpoints? Or perhaps you are performing an incident response investigation and need to gather all the logs to a centralized location? While using agents such as filebeat or Splunk Unvirsal Forwarders is still highly recommended but perhaps you are unable to install those agents on every endpoint. his is where the WEC shines! As more and more agents are being installed on endpoints you start running into a multitude of issue such as peformance issues, agents just not function correctly, or even management approval to do so. 



## Window-Event-Logging
List out the System audit policy<br />
Command: AuditPol /get /category:* <br /><br />
To set an item:<br />
Auditpol /set /category:"Account Management"<br />
/success:enable /failure:enable<br /><br />
To set a subcategory individually:<br />
Auditpol /set /subcategory:"Directory Service Access"<br />
/success:disable /failure:disable<br />

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

https://learn.microsoft.com/en-us/windows/win32/wec/windows-event-collector
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
