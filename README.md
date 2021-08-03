# Active-DIrectory
This Repository will contains various tools,scripts,commands used in Active Directory Enumeration


## Domain Enumeration

# Computer Objects Enumeration

```
Get-NetComputer : It will list down all the computer object in the domain
Get-Netcomputer -FullData : It will list down all the properties of all computer objects in the domain.
Get-Netcomputer -OperatingSystem "*Server 2016*" : It will list down all the computer objects having Server 2016 as their operating system.
Get-Netcomputer -FullData | select OperatingSystem : It will list down all the OperatingSystem Property of all the computer objects.
Get-Netcomputer -Ping : It will check which of the computer objects are live in the domain.

```

# Group Enumeration

```
Get-NetGroup: It will list down all the groups 
Get-Netgroup 'Domain Admin' : It will check whether the Domain Admin group exists or not.
Get-Netgroup -GroupName "*admin*": It will return all those groups whose name contain the word "admin".
Get-NetgroupMember -groupname 'Domain Admin' : It will list down the members of the domain admins.

