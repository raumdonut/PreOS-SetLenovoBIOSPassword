# Set a Supervisorpassword on Lenovo Thinkpads
> [! WARNING]  
> This is currently a PoC and needs testing. Works only for Matrix42 Empirum.

> [! IMPORTANT]  
> Import the PreOS Package into your Matrix42 Environment.  
> [Import PreOS Packages](https://help.matrix42.de/010_SUEM/020_UEM/20Client_Management/OS_Deployment/WinPE/2_WinPE_konfigurieren#Via_Matrix42_Marketplace)  
> The Thinkpad must be booted via PXE in System Deployment Boot Mode.  
> Learn more here: [Lenovo CDRT SDBM](https://docs.lenovocdrt.com/ref/bios/sdbm/#activating-system-deployment-boot-mode)

A PreOS Package for Matrix42 Empirum to initially set the BIOS Supervisor Password on Lenovo Thinkpads.  

We use the System Deployment Boot Mode introduced on the Thinkpad T490 (Comet Lake) to set an initial supervisorpassword. Here you can find an overview of the supported models:[Supported Models](https://docs.lenovocdrt.com/ref/bios/sdbm/#supported-systems)
> [!CAUTION]  
> This only works on Thinkpads with no Supevisorpassword set!

## Download and Usage
1. Clone the Repo 
2. Please extract the archive to `%EmpirumServer%\Configurator$\PackageStore\PreOSPackages` and import the package into your Software Depot (Matrix42 Management Console > Configuration > Depot).
3. Move the package within the depot register "Matrix42 PreOS Packages" before the "WindowsInstallation" package and activate it for deployment ("Ready to install").
4. Then you can assign the package and set the package variable to set a new BIOS Password.