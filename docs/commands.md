### Power shell commands to collect event logs.

```powershell

Get-EventLog  -Newest 50 -LogName Application | Format-Table
Get-EventLog  -Newest 50 -LogName Application | Format-Table Message -Wrap
Get-EventLog -EntryType "Error"  -Newest 30 -LogName Application | Format-Table
Get-EventLog -EntryType "Error"  -Newest 30 -LogName Application | Format-Table Message -Wrap

```