# Set a supervisor password on Lenovo Thinkpads
> [!CAUTION]  
> This is currently a Proof of Concept (PoC) and needs testing. It works only for Matrix42 Empirum.

> [!IMPORTANT]  
> Import the PreOS Package into your Matrix42 Environment.
> [Import PreOS Packages](https://help.matrix42.de/010_SUEM/020_UEM/20Client_Management/OS_Deployment/WinPE/2_WinPE_konfigurieren#Via_Matrix42_Marketplace)  
> The ThinkPad must be booted via PXE in System Deployment Boot Mode. 
> Learn more here: [Lenovo CDRT SDBM](https://docs.lenovocdrt.com/ref/bios/sdbm/#activating-system-deployment-boot-mode)

A PreOS Package for Matrix42 Empirum to initially set the BIOS supervisor password on Lenovo ThinkPads.

We use the System Deployment Boot Mode introduced on the ThinkPad T490 (Comet Lake) to set an initial supervisor password. Here you can find an overview of the supported models: [Supported Models](https://docs.lenovocdrt.com/ref/bios/sdbm/#supported-systems)
> [!CAUTION]  
> This only works on Thinkpads with no Supervisorpassword set!

## Features
- checks if the device is from lenovo. If not it exits.
- checks via an array if the model is not supported:  
  "$notSupportedList" which is currently populated with t480s/t490s modelnames. Add more unsupported models in your environment
- sets the BIOS password. The BIOS password is set via the package variable “LenovoBIOSPW”.

## Download and Usage
1. Clone the repository.
2. Extract the archive to %EmpirumServer%\Configurator$\PackageStore\PreOSPackages and import the package into your Software Depot (Matrix42 Management Console > Configuration > Depot).
3. Move the package within the depot register "Matrix42 PreOS Packages" before the "Windows Installation" package and activate it for deployment ("Ready to install").
4. Then you can assign the package and set the package variable to configure a new BIOS Password.
