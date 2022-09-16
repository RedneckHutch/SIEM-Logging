# SIEM-Logging

- [Window Event Logging](#Window-Event-Logging)
- [SYSMON-Logging](#SYSMON)
- [DNS Logging](#DNS-Logging)
- [Resources](#Resources)

## Window-Event-Logging
List out the System audit policy
 Command: AuditPol /get /category:*
To set an item:
 Auditpol /set /category:"Account Management"
/success:enable /failure:enable
To set a subcategory individually:
 Auditpol /set /subcategory:"Directory Service Access"
/success:disable /failure:disable

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
