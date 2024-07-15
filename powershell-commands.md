# Comprehensive List of powershell Commands

## Basic Commands

### `Get-Help`
Displays information about powershell commands and concepts.
```powershell
Get-Help <cmdlet>
```
Example:
```powershell
Get-Help Get-Process
```

### Get-Command
Gets all commands, including cmdlets, functions, aliases, and scripts.

```powershell
Get-Command
```
Example:
```powershell
Get-Command -Name *Service*
```

### Get-Process
Gets the processes that are running on the local computer or a remote computer.

```powershell
Get-Process
```
Example:
```powershell
Get-Process
```
### Start-Process
Starts one or more processes on the local computer.

```powershell
Start-Process <application>
```
Example:
```powershell
Start-Process notepad.exe
```
### Stop-Process
Stops one or more running processes.

```powershell
Stop-Process -Name <processname>
```
Example:
```powershell
Stop-Process -Name notepad
```
### Get-Service
Gets the status of services on a local or remote computer.

```powershell
Get-Service
```
Example:
```powershell
Get-Service
```
### Start-Service
Starts one or more stopped services.

```powershell
Start-Service -Name <servicename>
```
Example:
```powershell
Start-Service -Name W32Time
```
### Stop-Service
Stops one or more running services.

```powershell
Stop-Service -Name <servicename>
```
Example:
```powershell
Stop-Service -Name W32Time
```
### Restart-Service
Stops and then starts one or more services.

```powershell
Restart-Service -Name <servicename>
```
Example:
```powershell
Restart-Service -Name W32Time
```
### Set-Service
Starts, stops, and suspends a service, and changes its properties.

```powershell
Set-Service -Name <servicename> -Status <status>
```
Example:
```powershell
Set-Service -Name W32Time -Status Running
```
### Get-EventLog
Gets the events in the event log on the local or remote computers.

```powershell
Get-EventLog -LogName <logname>
```
Example:
```powershell
Get-EventLog -LogName System
```

### Write-Output
Sends the specified objects to the next command in the pipeline.

```powershell
Write-Output <string>
```
Example:
```powershell
Write-Output "Hello, World!"
```

### Write-Host
Displays objects to the host.

```powershell
Write-Host <string>
```
Example:
```powershell
Write-Host "Hello, World!"
```

### Write-Error
Writes an error message to the error stream.

```powershell
Write-Error <message>
```
Example:
```powershell
Write-Error "An error occurred."
```

### Write-Warning
Writes a warning message to the warning stream.

```powershell
Write-Warning <message>
```
Example:
```powershell
Write-Warning "This is a warning."
```

### Write-Debug
Writes a debug message to the debug stream.

```powershell
Write-Debug <message>
```
Example:
```powershell
Write-Debug "Debugging information."
```

### Write-Verbose
Writes a verbose message to the verbose stream.

```powershell
Write-Verbose <message>
```
Example:
```powershell
Write-Verbose "Verbose output."
```

## File and Directory Commands
Get-ChildItem
Gets the items and child items in one or more specified locations.

```powershell
Get-ChildItem -Path <path>
```
Example:
```powershell
Get-ChildItem -Path C:\Windows
```

### Set-Location
Sets the current working location to a specified location.

```powershell
Set-Location -Path <path>
```
Example:
```powershell
Set-Location -Path C:\Windows
```

### Copy-Item
Copies an item from one location to another.

```powershell
Copy-Item -Path <source> -Destination <destination>
```
Example:
```powershell
Copy-Item -Path C:\file.txt -Destination D:\backup\file.txt
```

### Move-Item
Moves an item from one location to another.

```powershell
Move-Item -Path <source> -Destination <destination>
```
Example:
```powershell
Move-Item -Path C:\file.txt -Destination D:\backup\file.txt
```

### Remove-Item
Deletes the specified items.

```powershell
Remove-Item -Path <path>
```
Example:
```powershell
Remove-Item -Path C:\file.txt
```

### New-Item
Creates a new item in a specified location.

```powershell
New-Item -Path <path> -ItemType <type>
```
Example:
```powershell
New-Item -Path C:\NewFolder -ItemType Directory
```

### Rename-Item
Renames an item in a specified location.

```powershell
Rename-Item -Path <path> -NewName <newname>
```
Example:
```powershell
Rename-Item -Path C:\file.txt -NewName newfile.txt
```

## Network Commands

### Test-Connection
Sends ICMP echo request packets ("pings") to one or more computers.

```powershell
Test-Connection -ComputerName <name or IP>
```
Example:
```powershell
Test-Connection -ComputerName google.com
```

### Get-NetIPAddress
Gets the IP address configuration.

```powershell
Get-NetIPAddress
```

### Get-NetAdapter
Gets the basic network adapter properties.

```powershell
Get-NetAdapter
```

### Get-NetRoute
Gets IP route information from the IP routing table.

```powershell
Get-NetRoute
```

### New-NetIPAddress
Creates and configures an IP address.

```powershell
New-NetIPAddress -InterfaceAlias <alias> -IPAddress <ip> -PrefixLength <length>
```
Example:
```powershell
New-NetIPAddress -InterfaceAlias Ethernet -IPAddress 192.168.1.10 -PrefixLength 24
```

## User and Group Management Commands
Get-LocalUser
Gets local user accounts.

```powershell
Get-LocalUser
```

### New-LocalUser
Creates a local user account.

```powershell
New-LocalUser -Name <username> -Password (ConvertTo-SecureString -AsPlainText "<password>" -Force)
```
Example:
```powershell
New-LocalUser -Name johndoe -Password (ConvertTo-SecureString -AsPlainText "Pa$$w0rd" -Force)
```

### Set-LocalUser
Changes the properties of a local user account.

```powershell
Set-LocalUser -Name <username> -Password (ConvertTo-SecureString -AsPlainText "<newpassword>" -Force)
```
Example:
```powershell
Set-LocalUser -Name johndoe -Password (ConvertTo-SecureString -AsPlainText "N3wPa$$w0rd" -Force)
```

### Remove-LocalUser
Deletes a local user account.

```powershell
Remove-LocalUser -Name <username>
```
Example:
```powershell
Remove-LocalUser -Name johndoe
```

### Get-LocalGroup
Gets local group accounts.

```powershell
Get-LocalGroup
```

### New-LocalGroup
Creates a local group.

```powershell
New-LocalGroup -Name <groupname>
```
Example:
```powershell
New-LocalGroup -Name PowerUsers
```

### Set-LocalGroup
Changes the properties of a local group.

```powershell
Set-LocalGroup -Name <groupname> -Description "<description>"
```
Example:
```powershell
Set-LocalGroup -Name PowerUsers -Description "Power Users Group"
```

### Remove-LocalGroup
Deletes a local group.

```powershell
Remove-LocalGroup -Name <groupname>
```
Example:
```powershell
Remove-LocalGroup -Name PowerUsers
```

### Add-LocalGroupMember
Adds members to a local group.

```powershell
Add-LocalGroupMember -Group <groupname> -Member <username>
```
Example:
```powershell
Add-LocalGroupMember -Group Administrators -Member johndoe
```

### Remove-LocalGroupMember
Removes members from a local group.

```powershell
Remove-LocalGroupMember -Group <groupname> -Member <username>
```
Example:
```powershell
Remove-LocalGroupMember -Group Administrators -Member johndoe
```

## Security and Permissions Commands
Get-Acl
Gets the security descriptor for a resource, such as a file or registry key.

```powershell
Get-Acl -Path <path>
```
Example:
```powershell
Get-Acl -Path C:\file.txt
```

### Set-Acl
Sets the security descriptor of a resource, such as a file or registry key.

```powershell
Set-Acl -Path <path> -AclObject <acl>
```
Example:
```powershell
$acl = Get-Acl -Path C:\file.txt
$acl.SetOwner([System.Security.Principal.NTAccount]"Administrator")
Set-Acl -Path C:\file.txt -AclObject $acl
```

### Get-Item
Gets the item at the specified location.

```powershell
Get-Item -Path <path>
```
Example:
```powershell
Get-Item -Path C:\file.txt
```

### Set-Item
Changes the value of an item to the value specified in the command.

```powershell
Set-Item -Path <path> -Value <value>
```
Example:
```powershell
Set-Item -Path HKCU:\Software\Test -Value "New Value"
```

### New-ItemProperty
Creates a new property for an item and sets its value.

```powershell
New-ItemProperty -Path <path> -Name <name> -Value <value>
```
Example:
```powershell
New-ItemProperty -Path HKCU:\Software\Test -Name "TestProperty" -Value "TestValue"
```

### Remove-ItemProperty
Deletes a property and its value from an item.

```powershell
Remove-ItemProperty -Path <path> -Name <name>
```
Example:
```powershell
Remove-ItemProperty -Path HKCU:\Software\Test -Name "TestProperty"
```

## Registry Commands
Get-ItemProperty
Gets the properties of an item at the specified location.

```powershell
Get-ItemProperty -Path <path>
```
Example:
```powershell
Get-ItemProperty -Path HKCU:\Software\Test
```

### Set-ItemProperty
Sets the value of a property at the specified location.

```powershell
Set-ItemProperty -Path <path> -Name <name> -Value <value>
```
Example:
```powershell
Set-ItemProperty -Path HKCU:\Software\Test -Name "TestProperty" -Value "NewValue"
```

### Remove-Item
Deletes the item at the specified location.

```powershell
Remove-Item -Path <path>
```
Example:
```powershell
Remove-Item -Path HKCU:\Software\Test
```

## Scripting Commands
Invoke-Expression
Runs a command or expression on the local computer.

```powershell
Invoke-Expression -Command <command>
```
Example:
```powershell
Invoke-Expression -Command "Get-Process | Out-File -FilePath C:\processes.txt"
```

### Invoke-Command
Runs commands on local and remote computers.

```powershell
Invoke-Command -ScriptBlock <scriptblock> -ComputerName <computer>
```
Example:
```powershell
Invoke-Command -ScriptBlock { Get-Process } -ComputerName RemotePC
```

### Start-Sleep
Suspends the activity in a script or session for the specified period of time.
```powershell
Start-Sleep -Seconds <seconds>
```
Example:
```powershell
Start-Sleep -Seconds 10
```

### New-ScriptFile
Creates a new script file.
```powershell
New-Item -Path <path> -ItemType File -Value <content>
```
Example:
```powershell
New-Item -Path C:\script.ps1 -ItemType File -Value "Write-Host 'Hello, World!'"
```

### Import-Module
Adds one or more modules to the current session.
```powershell
Import-Module <module>
```
Example:
```powershell
Import-Module ActiveDirectory
```

### Export-ModuleMember : 
Specifies the module members that are exported.
```powershell
Export-ModuleMember -Function <function>
```
Example:
```powershell
Export-ModuleMember -Function Get-Data
```

### Remove-Module : 
Removes modules from the current session.
```powershell
Remove-Module <module>
```
Example:
```powershell
Remove-Module ActiveDirectory
```

## Miscellaneous Commands

### Clear-Host
Clears the content displayed on the console.
```powershell
Clear-Host
```

### Measure-Object
Calculates the numeric properties of objects, and the characters, words, and lines in string objects, such as files of text.
```powershell
Measure-Object -Property <property> -Sum
```
Example:
```powershell
Measure-Object -Path C:\file.txt -Property Length -Sum
```

### Out-File
Sends output to a file.
```powershell
Out-File -FilePath <path>
```
Example:
```powershell
Get-Process | Out-File -FilePath C:\processes.txt
```

### Select-Object
Selects specified properties of an object or set of objects.
```powershell
Select-Object -Property <property>
```
Example:
```powershell
Get-Process | Select-Object -Property Name, Id
```

### Sort-Object
Sorts objects by property values.
```powershell
Sort-Object -Property <property>
```
Example:
```powershell
Get-Process | Sort-Object -Property Name
```

### Group-Object
Groups objects that contain the same value for specified properties.
```powershell
Group-Object -Property <property>
```
Example:
```powershell
Get-Process | Group-Object -Property Name
```

### Where-Object
Selects objects from a collection based on their property values.
```powershell
Where-Object { <condition> }
```
Example:
```powershell
Get-Process | Where-Object { $_.CPU -gt 100 }
```

### ForEach-Object
Performs an operation on each item in a collection of input objects.
```powershell
ForEach-Object { <scriptblock> }
```
Example:
```powershell
Get-Process | ForEach-Object { $_.Name }
```

### New-Alias
Creates a new alias.
```powershell
New-Alias -Name <alias> -Value <cmdlet>
```
Example:
```powershell
New-Alias -Name list -Value Get-ChildItem
```

### Get-Alias
Gets the aliases in the current session.
```powershell
Get-Alias
```

### Set-Alias
Creates or changes an alias.
```powershell
Set-Alias -Name <alias> -Value <cmdlet>
```
Example:
```powershell
Set-Alias -Name list -Value Get-ChildItem
```
