# SIEM-Logging

- [Window Event Logging](#Window-Event-Logging)
- [SYSMON-Logging](#SYSMON)
- [DNS Logging](#DNS-Logging)
- [Resources](#Resources)

## Window-Event-Logging
List out the System audit policy<br />
Command: AuditPol /get /category:* <br /><br />
To set an item:<br />
Auditpol /set /category:"Account Management"<br />
/success:enable /failure:enable<br /><br />
To set a subcategory individually:<br />
Auditpol /set /subcategory:"Directory Service Access"<br />
/success:disable /failure:disable<br />

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
