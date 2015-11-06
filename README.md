# Azure Automation PowerShell ISE Addon

## Description

The Azure Automation PowerShell ISE add on makes it easy to author and test your runbooks in your local PowerShell ISE.

**Note: This project is currently in development. Please open issues found or provide feedback in the feedback section of the add on.**

## Features
* Enables use of the Automation activities (Get-AutomationVariable, Get-AutomationPSCredential, etc) in local PowerShell Workflows
* Allows creating and editing the values of Automation assets locally
* Allows easy tracking of local changes to runbooks and assets vs the state of these items in an Azure Automation account
* Allows syncing of runbook / asset changes between a local runbook authoring environment and an Azure Automation account
* Allows testing of PowerShell workflow scripts locally in the ISE and also in the automation service without changing the runbook


## Installation

### From GitHub Releases
To install the latest build of the add-on, follow the instructions for our [Early adopter release](https://github.com/azureautomation/azure-automation-ise-addon/releases/tag/v0.2.2)

### From PowerShell Gallery
To install from PowerShell Gallery:
* Open the PowerShell console as an administrator
* Run `Install-Module AzureAutomationAuthoringToolkit`

If you want the PowerShell ISE to always automatically load the Azure Automation ISE addon:
* Run `Install-AzureAutomationIseAddOn`

If not:
* Any time you want to use the Azure Automation ISE addon in the PowerShell ISE, run `Import-Module AzureAutomationAuthoringToolkit` in the PowerShell ISE

### From Source
To build from source:
* [Download](https://github.com/azureautomation/azure-automation-ise-addon/archive/master.zip) or clone this repository, and extract from zip if necessary
* Open AutomationISE/AutomationISE.sln in Visual Studio
* Build the solution. NuGet will pull the required packages.
* Put the resulting binaries in the AzureAutomationAuthoringToolkit/ISEaddon directory
* Place the AzureAutomationAuthoringToolkit folder somewhere in your PSModulePath, ex: `C:\Users\<USERNAME>\Documents\WindowsPowerShell\Modules`

If you want the PowerShell ISE to always automatically load the Azure Automation ISE addon:
* Open the PowerShell ISE, and run `Install-AzureAutomationIseAddOn`
* The Azure Automation ISE add-on should appear on the right side of the PowerShell ISE:
![alt text](https://github.com/azureautomation/azure-automation-ise-addon/blob/master/Screenshots/Automation-Add-On.png " Azure Automation Add-On")
If not:
* Any time you want to use the Azure Automation ISE addon in the PowerShell ISE, run `Import-Module AzureAutomationAuthoringToolkit` in the PowerShell ISE


## Uninstallation

* Open the PowerShell console as an administrator
* Run `Uninstall-AzureAutomationIseAddOn`
* Run `Uninstall-Module AzureAutomationAuthoringToolkit`
* If the PowerShell ISE was open, reopen it
* From now on, opening the PowerShell ISE will no longer cause the Azure Automation ISE add-on to be loaded
