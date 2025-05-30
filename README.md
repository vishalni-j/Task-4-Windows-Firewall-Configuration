# Task-4-Windows-Firewall-Configuration

# Objective
To configure and test default firewall rules on a Windows system to learn how firewalls control and block network traffic.

# Tools Used
- Windows Defender Firewall
- PowerShell

# Steps Performed

1. Displayed Existing Firewall Rules
- Utilized PowerShell to show existing rules:
```powershell
Get-NetFirewallRule | Select-Object DisplayName, Direction, Action, Enabled, Profile
```
- Exported the list to a text file for documentation:
powershell
Get-NetFirewallRule | Select-Object DisplayName, Direction, Action, Enabled, Profile | Out-File "$env:USERPROFILE\Desktop\firewall_rules.txt"

2. Blocked Inbound Traffic on Port 23 (Telnet)
- Utilized the Windows Firewall GUI to establish a rule to block all incoming connections on port 23 (used for insecure Telnet).

3. Permitted SSH Port 
- Established a rule permitting traffic on port 22 (SSH), although less used in Windows systems.

4. Tested Rules
- Conducted test connections to verify if the block and permit rules were set accordingly.

5. Deleted Test Rules
- Removed the added rules to return the system to its original state.

#  Output File
- `firewall_rules.txt`: Holds exported firewall rules of the system after modifications have been made.

#  Key Concepts Covered
- Windows firewall rules view, addition, and deletion.
- Inbound versus outbound traffic regulation.
- Port-level rules' enhancement of system security.
- Basic usage of PowerShell for firewall functionalities.

