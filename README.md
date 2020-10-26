CMPE 283 – Homework #1	Hung Le
1. I completed the assignment myself.
2.

Step 1: Use VMWare to create a Guest Ubuntu OS

Step 2: After created an Ubuntu VM, run the VM and open the terminal inside the VM

Step 3: Run commands ‘cat /proc/cpuinfo’ to check flags ‘vmx’

Step 4: In the folder where the cmpe28301.c file located, run the following commands:
make
sudo insmod ./cmpe283-1.ko
sudo rmmod cmpe283-1
dmesg

Result: 
[11528.044840] CMPE 283 Assignment 1 Module Start
[11528.044842] Pinbased Controls MSR: 0x3f00000016
[11528.044843]   External Interrupt Exiting: Can set=Yes, Can clear=Yes
[11528.044844]   NMI Exiting: Can set=Yes, Can clear=Yes
[11528.044844]   Virtual NMIs: Can set=Yes, Can clear=Yes
[11528.044844]   Activate VMX Preemption Timer: Can set=No, Can clear=Yes
[11528.044845]   Process Posted Interrupts: Can set=No, Can clear=Yes
[11528.044846] Procbased Controls MSR: 0xfff9fffe0401e172
[11528.044846]    Interrupt-window exiting: Can set=Yes, Can clear=Yes
[11528.044847]    Use TSC offsetting: Can set=Yes, Can clear=Yes
[11528.044847]    HLT exiting: Can set=Yes, Can clear=Yes
[11528.044847]    INVLPG exiting: Can set=Yes, Can clear=Yes
[11528.044848]    MWAIT exiting: Can set=Yes, Can clear=Yes
[11528.044848]    RDPMC exiting: Can set=Yes, Can clear=Yes
[11528.044868]    RDTSC exiting: Can set=Yes, Can clear=Yes
[11528.044869]    CR3-load exiting: Can set=Yes, Can clear=No
[11528.044869]    CR3-store exiting: Can set=Yes, Can clear=No
[11528.044870]    CR8-load exiting: Can set=Yes, Can clear=Yes
[11528.044870]    CR8-store exiting: Can set=Yes, Can clear=Yes
[11528.044870]    Use TPR shadow : Can set=Yes, Can clear=Yes
[11528.044871]    NMI-window exiting: Can set=Yes, Can clear=Yes
[11528.044871]    MOV-DR exiting: Can set=Yes, Can clear=Yes
[11528.044871]    Unconditional I/O exiting: Can set=Yes, Can clear=Yes
[11528.044872]    Use I/O bitmaps : Can set=Yes, Can clear=Yes
[11528.044872]    Monitor trap flag : Can set=Yes, Can clear=Yes
[11528.044873]    Use MSR bitmaps : Can set=Yes, Can clear=Yes
[11528.044873]    MONITOR exiting : Can set=Yes, Can clear=Yes
[11528.044873]    PAUSE exiting: Can set=Yes, Can clear=Yes
[11528.044874]    Activate secondary controls : Can set=Yes, Can clear=Yes
[11528.044875] Secondary Procbased Controls MSR: 0x553cfe00000000
[11528.044875]    Virtualize APIC accesses: Can set=No, Can clear=Yes
[11528.044876]    Enable EPT: Can set=Yes, Can clear=Yes
[11528.044876]    Descriptor-table exiting: Can set=Yes, Can clear=Yes
[11528.044877]    Enable RDTSCP: Can set=Yes, Can clear=Yes
[11528.044877]    Virtualize x2APIC mode: Can set=Yes, Can clear=Yes
[11528.044877]    Enable VPID: Can set=Yes, Can clear=Yes
[11528.044878]    WBINVD exiting: Can set=Yes, Can clear=Yes
[11528.044878]    Unrestricted guest: Can set=Yes, Can clear=Yes
[11528.044879]    APIC-register virtualization: Can set=No, Can clear=Yes
[11528.044879]    Virtual-interrupt delivery: Can set=No, Can clear=Yes
[11528.044879]    PAUSE-loop exiting: Can set=Yes, Can clear=Yes
[11528.044880]    RDRAND exiting: Can set=Yes, Can clear=Yes
[11528.044880]    Enable INVPCID: Can set=Yes, Can clear=Yes
[11528.044880]    Enable VM functions: Can set=Yes, Can clear=Yes
[11528.044881]    VMCS shadowing : Can set=No, Can clear=Yes
[11528.044881]    Enable ENCLS exiting : Can set=No, Can clear=Yes
[11528.044882]    RDSEED exiting: Can set=Yes, Can clear=Yes
[11528.044882]    Enable PML: Can set=No, Can clear=Yes
[11528.044882]    EPT-violation #VE: Can set=Yes, Can clear=Yes
[11528.044883]    Conceal VMX from PT: Can set=No, Can clear=Yes
[11528.044883]    Enable XSAVES/XRSTORS: Can set=Yes, Can clear=Yes
[11528.044884]    Mode-based execute control for EPT: Can set=Yes, Can clear=Yes
[11528.044884]    Sub-page write permissions for EPT: Can set=No, Can clear=Yes
[11528.044885]    Intel PT uses guest physical addresses: Can set=No, Can clear=Yes
[11528.044885]    Use TSC scaling: Can set=No, Can clear=Yes
[11528.044885]    Enable user wait and pause: Can set=No, Can clear=Yes
[11528.044886]    Enable ENCLV exiting: Can set=No, Can clear=Yes
[11528.044887] Exit Controls MSR: 0xbfffff00036dff
[11528.044887]    Save debug controls: Can set=Yes, Can clear=No
[11528.044887]    Host address-space size: Can set=Yes, Can clear=Yes
[11528.044888]    Load IA32_PERF_GLOBAL_CTRL: Can set=Yes, Can clear=Yes
[11528.044888]    Acknowledge interrupt on exit: Can set=Yes, Can clear=Yes
[11528.044889]    Save IA32_PAT: Can set=Yes, Can clear=Yes
[11528.044889]    Load IA32_PAT: Can set=Yes, Can clear=Yes
[11528.044889]    Save IA32_EFER: Can set=Yes, Can clear=Yes
[11528.044890]    Load IA32_EFER: Can set=Yes, Can clear=Yes
[11528.044890]    Save VMXpreemption timer value: Can set=No, Can clear=Yes
[11528.044890]    Clear IA32_BNDCFGS: Can set=Yes, Can clear=Yes
[11528.044891]    Conceal VMX from PT: Can set=No, Can clear=Yes
[11528.044891]    Clear IA32_RTIT_CTL: Can set=No, Can clear=Yes
[11528.044892]    Load CET state: Can set=No, Can clear=Yes
[11528.044892]    Load PKRS: Can set=No, Can clear=Yes
[11528.044893] Entry Controls MSR: 0x1f3ff000011ff
[11528.044893]    Load debug controls: Can set=Yes, Can clear=No
[11528.044894]    IA-32e mode guest: Can set=Yes, Can clear=Yes
[11528.044894]    Entry to SMM: Can set=No, Can clear=Yes
[11528.044894]    Deactivate dualmonitor treatment: Can set=No, Can clear=Yes
[11528.044895]    Load IA32_PERF_GLOBAL_CTRL: Can set=Yes, Can clear=Yes
[11528.044895]    Load IA32_PAT: Can set=Yes, Can clear=Yes
[11528.044896]    Load IA32_EFER: Can set=Yes, Can clear=Yes
[11528.044896]    Load IA32_BNDCFGS: Can set=Yes, Can clear=Yes
[11528.044896]    Conceal VMX from PT: Can set=No, Can clear=Yes
[11528.044897]    Load IA32_RTIT_CTL: Can set=No, Can clear=Yes
[11528.044897]    Load CET state: Can set=No, Can clear=Yes
[11528.044897]    Load PKRS: Can set=No, Can clear=Yes
[11531.866741] CMPE 283 Assignment 1 Module Exits

