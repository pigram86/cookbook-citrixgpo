Description
===========

This cookbook is for the scripted install of Group Policy Objects releated to a Citrix environment. Author Ron Oberjohann created the POSH code. I provided the GPOs and the performed the Chef conversion.

From Ron's POSH Scripts:
------------------------
* For more information on the CMDlets used see http://technet.microsoft.com/en-us/library/ee461034.aspx & http://technet.microsoft.com/en-us/library/ee461027.aspx
*  Special thanks to Todd Pigram @ http://www.toddpigram.com for the base GPO's to collect recommended settings
* Group Policy Cmdlet Prerequisites
* To use the Windows PowerShell cmdlets for Group Policy, you must be running one of the following: 
* Windows Server 2008 R2 on a domain controller
* --or--
* Windows Server 2008 R2 on a member server that has the GPMC installed
* --or--
* Windows® 7 with Remote Server Administration Tools (RSAT) installed. (RSAT includes the GPMC and the Group Policy cmdlets)

* Always test scripts in a non production affecting method!
* Use at your own risk! The author is NOT responsible for any damages.

* This script does not link to any AD object by default.
* For more information about linking the GPO see http://technet.microsoft.com/en-us/library/ee461061.aspx

* An Example of the command used
* Set-GPRegistryValue -Name "TestGPO" -key "HKCU\Software\Policies\Microsoft\ExampleKey" -ValueName "ValueOne", "ValueTwo", "ValueThree" 
* Cannot string DWORD VALUES

Supported Platforms
===================

* Windows Server 2008 R2
* Windows Server 2012
* Windows Server 2012 R2

Cookbooks
=========

* windows
* powershell



Usage
=====

* These recipes will be use to create GPOs for a Citrix Environment. Assignment of the created GPO are as follows:
* citrix_gpo::CtxDefaultPolicy - Assigned to top level Citrix OU
* citrix_gpo::CtxUPM - Assigned to Session Hosts
* citrix_gpo::CtxStartMenu - Assigned to Users 
* citrix_gpo::CtxPersonalizedUser - Assigned to Users 
* citrix_gpo::CtxAppConfig - Assigned to Users 
* citrix_gpo::CtxRestrictedUser - Assigned to Users 
* citrix_gpo::CtxRestrictedComputer - Assigned to Users 

Contributing
============

1. Fork the repository on Github
2. Create a named feature branch (i.e. `add-new-recipe`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request

License and Authors
===================

* Author:: Todd Pigram (<todd@toddpigram.com>)
* Author:: Ron Oberjohann (<ron@advdat.com>)

Copyright:: 2014, Todd Pigram

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

