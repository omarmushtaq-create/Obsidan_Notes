## Using PowerShell

In enterprise environments, PowerShell is quite often used to develop scripts to create virtual machines. When using PowerShell, the process typically consists of using three cmdlets.

The first cmdlet is `New-VM` which sets up the new virtual machine, defines its basic properties (name, generation), where to store its files, how much memory it starts with, and the configuration of its virtual hard disk. The common switches used with this cmdlet include:

- `-Name`: Specifies the name of the new VM.
- `-Path`: Sets the location on disk where the VM configuration files will be stored.
- `-MemoryStartupBytes`: Defines how much memory (RAM) the VM starts with when it is powered on. You can specify values like `1024MB`, `2GB`, etc.
- `-Generation`: Specifies the VM generation (for example, `1` or `2`), which determines supported features and hardware.
- `-VHDPath`: Points to the location where the virtual hard disk file (VHD/VHDX) is or will be stored.
- `-VHDSizeBytes`: Defines the size of the virtual hard disk that will be created for the VM.

Once the VM is created, you can modify additional configuration settings with the `Set-VM` cmdlet. Common switches used with this cmdlet include:

- `-Name`: Identifies which VM you want to modify.
- `-DynamicMemoryEnabled`: Enables or disables dynamic memory for that VM:
    - `$true`: dynamic memory is enabled.
    - `$false`: dynamic memory is disabled.
- `-MemoryMinimumBytes`: When dynamic memory is enabled, this defines the minimum amount of memory the VM is allowed to use.
- `-MemoryMaximumBytes`: When dynamic memory is enabled, this defines the maximum amount of memory the VM can grow to.

Lastly, you will want to connect the new VM's virtual network adapter to a virtual switch. This is done using the `Connect-VMNetworkAdapter` cmdlet. The main switches used with this cmdlet include:

- `-VMName`: Specifies which VM’s network adapter you’re configuring.
- `-SwitchName`: Specifies which virtual switch the VM’s network adapter should connect to (for example, an internal, external, or private virtual switch).