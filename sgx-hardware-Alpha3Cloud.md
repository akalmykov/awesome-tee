SGX-hardware util output on an Alpha3Cloud instance:

```ssh
cloudsigma@sgx:~/SGX-hardware$ sudo ./test-sgx 
Start test-sgx
CPUID is available
The CPU is Genuine Intel
CPUID is capable of examining SGX capabilities
CPU: Intel(R) Xeon(R) Gold 6348 CPU @ 2.60GHz
  Stepping 6         Model 10           Family 6 
  Processor type 0   Extended model 6   Extended family 0 
Safer Mode Extensions (SMX): 0
Extended feature bits (EAX=7, ECX=0): eax: 00000000  ebx: f1bf07af  ecx: 40415f5e  edx: ac000410
Supports SGX
SGX Launch Configuration (SGX_LC): 1
SGX Attestation Services (SGX_KEYS): 0
SGX1 leaf instructions (SGX1): 1
SGX2 leaf instructions (SGX2): 1
EINCVIRTCHILD, EDECVIRTCHILD, and ESETCONTEXT (OVERSUB-VMX): 0
ETRACKC, ERDINFO, ELDBC, and ELDUC (OVERSUB-Supervisor): 0
EVERIFYREPORT2: 0
Allow attestation w/ updated microcode (EUPDATESVN): 0
Allow enclave thread to decrement TCS.CSSA (EDECCSSA): 0
Supported Extended features for MISC region of SSA (MISCSELECT) 0x00000001
The maximum supported enclave size in non-64-bit mode is 2^31
The maximum supported enclave size in     64-bit mode is 2^56
Raw ECREATE SECS.ATTRIBUTES[63:0]: 00000000 000000b6
    ECREATE SECS.ATTRIBUTES[DEBUG] (Debugger can read/write enclave data w/ EDBGRD/EDBGWR): 1
    ECREATE SECS.ATTRIBUTES[MODE64BIT] (Enclave can run as 64-bit): 1
    ECREATE SECS.ATTRIBUTES[PROVISIONKEY] (Provisioning key available from EGETKEY): 1
    ECREATE SECS.ATTRIBUTES[EINITTOKEN_KEY] (EINIT token key available from EGETKEY): 1
    ECREATE SECS.ATTRIBUTES[CET] (Enable Control-flow Enforcement Technology in enclave): 0
    ECREATE SECS.ATTRIBUTES[KSS] (Key Separation and Sharing Enabled): 1
    ECREATE SECS.ATTRIBUTES[AEXNOTIFY] (Threads may receive AEX notifications): 0
Raw ECREATE SECS.ATTRIBUTES[127:64] (XFRM: Copy of XCR0): 00000000 000002e7
EPC[0]: Protection: c   Base phys addr: 0000000100000000  size: 0000000040000000
vDSO base address: 0x7ffd6811c000
Printing Symbol Table:
vDSO symbol: __vdso_time
vDSO symbol: getcpu
vDSO symbol: __vdso_clock_getres
vDSO symbol: __vdso_getcpu
vDSO symbol: clock_getres
vDSO symbol: __vdso_gettimeofday
vDSO symbol: LINUX_2.6
vDSO symbol: gettimeofday
vDSO symbol: __vdso_clock_gettime
vDSO symbol: time
vDSO symbol: __vdso_sgx_enter_enclave
vDSO symbol: clock_gettime
Raw IA32_FEATURE_CONTROL: 0000000000160005
    IA32_FEATURE_CONTROL.LOCK_BIT[bit 0]: 1
    IA32_FEATURE_CONTROL.SGX_LAUNCH_CONTROL[bit 17] (Is the SGX LE PubKey writable?): 1
    IA32_FEATURE_CONTROL.SGX_GLOBAL_ENABLE[bit 18]: 1
The SGX Launch Enclave Public Key Hash can be changed
IA32_SGXLEPUBKEYHASH: a6053e051270b7ac 6cfbe8ba8b3b413d c4916d99f2b3735d d4f8c05909f9bb3b
IA32_SGX_SVN_STATUS not readable
MSR_SGXOWNEREPOCH not readable
XSAVE features and state-components
  Maximum size (in bytes) of current XCR0 XSAVE area: 2696
  Maximum size (in bytes) of all-set XCR0 XSAVE area: 2696
  Size (in bytes) of current XCR0+IA32_XSS XSAVE area: 2440
  Supported XCR0:     00000000000002e7
  Actual    XCR0:     00000000000002e7
  Supported IA32_XSS: 0000000000000000
  Actual    IA32_XSS: 0000000000000000
    Register Name    Supported Value Description
    ======== ======= ========= ===== ===========
    XCR0     x87:       yes      set x87 Floating Point Unit & MMX
    XCR0     SSE:       yes      set MXCSR and XMM registers
    XCR0     AVX:       yes      set YMM registers
    XCR0     BNDREG:     no    clear MPX for BND registers
    XCR0     BNDCSR:     no    clear MPX for BNDCFGU and BNDSTATUS registers
    XCR0     opmask:    yes      set AVX-512 for AVX opmask and AKA k-mask
    XCR0     ZMM_hi256: yes      set AVX-512 for the upper-halves of lower ZMM registers
    XCR0     Hi16_ZMM:  yes      set AVX-512 for the upper ZMM registers
    IA32_XSS PT:         no    clear Processor Trace
    XCR0     PKRU:      yes      set User Protection Keys
    IA32_XSS PASID:      no    clear Process Address Space ID
    IA32_XSS CET_U:      no    clear Control-flow Enforcement Technology: user-mode functionality MSRs
    IA32_XSS CET_S:      no    clear CET: shadow stack pointers for rings 0,1,2
    IA32_XSS HDC:        no    clear Hardware Duty Cycling
    IA32_XSS UINTR:      no    clear User-Mode Interrupts
    IA32_XSS LBR:        no    clear Last Branch Record
    IA32_XSS HWP:        no    clear Hardware P-state control
    XCR0     TILECFG:    no    clear AMX - Advanced Matrix Extensions
    XCR0     TILEDATA:   no    clear AMX - Advanced Matrix Extensions
    XCR0     APX:        no    clear Extended General Purpose Registers R16-R31
  Supported XSAVE feature flags: 0000000f
    xsaveopt - save state-components that have been modified since last XRSTOR: 1
    xsavec - save/restore state with compaction: 1
    xgetbv_ecx1 - XGETBV with ECX=1 support: 1
    xss - save/restore state with compaction, including supervisor state: 1
    xfd - Extended Feature Disable supported: 0
End test-sgx
```
