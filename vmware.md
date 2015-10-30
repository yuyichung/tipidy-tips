# VMWare

- ESXi: If you can't connect to the server via web service or vSphere client, SSH onto the server and check hostd & vpxa
- ESXi: /etc/init.d/hostd may look for keyword "localhost" in /etc/hosts. If hostd fails to start, check /etc/hosts
- How to enable nested VMs on an ESXi 5.1 (or higher) host: 
    1. Ensure that your hardware supports hardware virtualization(?)
    2. ssh into the ESXi host, find the .vmx file for the VM in which you wish to host nested VM
    3. Add "vhv.enable = "TRUE"" to the .vmx file
    4. Get the VMID of the VM by finding it from command "vim-cmd vmsvc/getallvms"
    5. Reload the VM's .vmx file with "vim-cmd vmsvc/reload Vmid"