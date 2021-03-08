# Reset-Logs

## What is Reset-Logs

Reset-Logs is a small utility that takes a log file (that must not be locked) and,

* [Optionally] Moves it into an archived state under a different name
* [Optionally] Emails it to a particular address
* Recreates it with an [Optional] Header

## History of Reset-Logs

Initially Reset-Logs was part of the UPS Monitoring utility (https://github.com/chribonn/UPSMonitor) but has now been extracted into its own repository because it can be used standalone in other solutions that would benefir from log file recycling.

The most uptodate version of this utility can be downloaded from https://github.com/chribonn/UPSMonitor

## PowerShell 7

Reset-Logs was tested on PowerShell 7. This version of PowerShell does not come installed by default on Windows.

Information on how to install this version is available on the  Microsoft page [Installing PowerShell on Windows](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-7.1)


## Configure Powershell execution policy if you get a PSSecurityException error

If you get an error when you execute the script similar to the one herunder you need to change the execution policy.

    .\Reset-Logs.ps1 : File .\Reset-Logs.ps1 cannot be loaded because running scripts is disabled on this system. For more information, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.

    At line:1 char:1
    + .\Reset-Logs.ps1 -help
    + ~~~~~~~~~~~~~~~~
        + CategoryInfo          : SecurityError: (:) [], PSSecurityException
        + FullyQualifiedErrorId : UnauthorizedAccess
	
Open Powershell as administrator and execute the following

    Set-ExecutionPolicy -ExecutionPolicy RemoteSigned


## Contact information

Feel free to fork this project and improve it.  If you would like to join the effort to make improvements contact me on chribonn@gmail.com.
