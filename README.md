# SIEM-Logging

- [Window Event Collector](#Window-Event-Collector)
- [Window Event Logging](#Window-Event-Logging)
- [SYSMON-Logging](#SYSMON)
- [DNS Logging](#DNS-Logging)

## Window-Event-Collector
Test
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
</table>
