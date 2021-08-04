# Active-DIrectory
This Repository will contains various tools,scripts,commands used in Active Directory Enumeration


# Domain Enumeration

## User Enumeration
Get-Domain Policy
Get-netdomain
Get-NetdomainController

Get-netuser
Get-netuser -username test123
Get-NetLoggedon -Computername server16 : It will tell all the users which are actively logged on to the computer.
Get-loggedonLocally : It will list all users who are logged in locally on the computer.
Get-LastLoggedon -Computername server016 : It will list user which have last logged on to the computer.
## Computer Objects Enumeration

```
Get-NetComputer : It will list down all the computer object in the domain
Get-Netcomputer -FullData : It will list down all the properties of all computer objects in the domain.
Get-Netcomputer -OperatingSystem "*Server 2016*" : It will list down all the computer objects having Server 2016 as their operating system.
Get-Netcomputer -FullData | select OperatingSystem : It will list down all the OperatingSystem Property of all the computer objects.
Get-Netcomputer -Ping : It will check which of the computer objects are live in the domain.

```

## Group Enumeration

```
Get-NetGroup: It will list down all the groups 
Get-Netgroup 'Domain Admin' : It will check whether the Domain Admin group exists or not.
Get-Netgroup -GroupName "*admin*": It will return all those groups whose name contain the word "admin".
Get-NetgroupMember -groupname 'Domain Admin' : It will list down the members of the domain admins.

