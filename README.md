# Download: https://git.io/wmie2


WMI Explorer is a utility intended to provide the ability to browse and view WMI namespaces/classes/instances/properties in a single pane of view and is inspired by the PowerShell based WMI Explorer written by Marc.

As someone who works with Configuration Manager (SCCM), I spend a lot of time in wbemtest trying to find things which is very time consuming. I started this project with the intention to combine the features of currently available WMI Explorers, and to make it easier and quicker to find what you're looking for in WMI.

# Requirements

* Microsoft .NET Framework 4.8
* Minimum display resolution: 1024x768
* Administrator rights to view some WMI objects
* (Optional) Internet access for automatic update check

# New Features as of 2.0.1.x
* Invoke WMIExplorer from command line:  
`WmiExplorer.exe HOSTNAME`  
`WmiExplorer.exe HOSTNAME USERNAME`  
`WmiExplorer.exe HOSTNAME USERNAME PASSWORD`   
I don't really recommend you use plaintext passwords on the command line.
* Generic support for method parameters that are arrays -- needs more testing as it is a somewhat primitive implementation.
* Script Generation updated to show CIM cmdlets and include legact WMI equivalents.
* Support for CSV export of methods.
* More to come.
# Features
* Browse and view WMI objects in a single pane of view.
* Connect as alternate credentials to remote computers.
* Asynchronous and Synchronous mode for enumeration.
* Method execution.
* SMS (Configuration Manager) mode providing additional functionality for Configuration Manager.
* Filter classes and instances matching specified criteria.
* View classes/instances in Managed Object Format (MOF).
* Search classes, methods and properties for names matching specified criteria.
* Run WQL queries.
* Automatic generation of WQL query for the selected Class/Instance.
* Automatic script creation (PowerShell and VBS).
* Highlighting enumerated objects.
* Display property descriptions and possible enumeration values (if available).
* Display methods descriptions and parameters.
* Display embedded property values.
* Caching enumerated classes/instances.
* View WMI Provider Process Information.
* Automatic check for new version.

# Known Issues

* Asynchronous mode currently applies only for Class and Instance enumeration. Search and Query execution is synchronous.
* Cached instance is not updated after clicking on ‘Refresh Object’.
* root\directory\LDAP namespace is excluded from Search because enumeration of objects in this namespace can take a very long time and can even return "Quota Violation" error.
* Scripting: PowerShell script execution through WMI Explorer requires PowerShell v2.
* Method Execution: Methods requiring input parameters of Object or Reference data type are currently not supported.
