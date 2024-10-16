Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
A process has executed an operation involving a call
to the fork() system call to create a child process.

As a result, the libfabric EFA provider is operating in
a condition that could result in memory corruption or
other system errors.

For the libfabric EFA provider to work safely when fork()
is called, you will need to set the following environment
variable:
RDMAV_FORK_SAFE

However, setting this environment variable can result in
signficant performance impact to your application due to
increased cost of memory registration.

You may want to check with your application vendor to see
if an application-level alternative (of not using fork)
exists.

Your job will now abort.
[fv-az1020-199:05914] *** Process received signal ***
[fv-az1020-199:05914] Signal: Aborted (6)
[fv-az1020-199:05914] Signal code:  (-6)
[fv-az1020-199:05914] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f563d642520]
[fv-az1020-199:05914] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f563d6969fc]
[fv-az1020-199:05914] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f563d642476]
[fv-az1020-199:05914] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f563d6287f3]
[fv-az1020-199:05914] [ 4] /lib/x86_64-linux-gnu/libfabric.so.1(+0x76b4e)[0x7f56222b4b4e]
[fv-az1020-199:05914] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0xeaf48)[0x7f563d6eaf48]
[fv-az1020-199:05914] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_fork+0x71)[0x7f563d6ea711]
[fv-az1020-199:05914] [ 7] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10SubprocessC2ERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xc1)[0x7f563ed87eb1]
[fv-az1020-199:05914] [ 8] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD14GenericMolInfo15interpretSymbolERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt6vectorINS_10AtomNumberESaISA_EE+0x162b)[0x7f563e65801b]
[fv-az1020-199:05914] [ 9] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD15ActionAtomistic17interpretAtomListERSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERKS1_IPNS_5ValueESaISC_EEPNS_6ActionERS1_INS_10AtomNumberESaISJ_EE+0x6c1)[0x7f563e5de9e1]
[fv-az1020-199:05914] [10] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD15ActionAtomistic13parseAtomListERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEiRSt6vectorINS_10AtomNumberESaISA_EE+0x10d)[0x7f563e5dff5d]
[fv-az1020-199:05914] [11] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD7generic14WholeMoleculesC1ERKNS_13ActionOptionsE+0x251)[0x7f563e866751]
[fv-az1020-199:05914] [12] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD18ActionRegistrationINS_7generic14WholeMoleculesEE6createERKNS_13ActionOptionsE+0x27)[0x7f563e868df7]
[fv-az1020-199:05914] [13] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD14ActionRegister6createERKSt6vectorIPvSaIS2_EERKNS_13ActionOptionsE+0x3f9)[0x7f563e5e3389]
[fv-az1020-199:05914] [14] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain14readInputWordsERKSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERKb+0x2da)[0x7f563e66b60a]
[fv-az1020-199:05914] [15] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain13readInputFileERNS_5IFileE+0x5c)[0x7f563e66bdbc]
[fv-az1020-199:05914] [16] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain13readInputFileERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0x9f)[0x7f563e6714cf]
[fv-az1020-199:05914] [17] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain4initEv+0xb6a)[0x7f563e6720aa]
[fv-az1020-199:05914] [18] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain3cmdESt17basic_string_viewIcSt11char_traitsIcEERKNS_11TypesafePtrE+0x29bf)[0x7f563e67504f]
[fv-az1020-199:05914] [19] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD7cltools6DriverIdE4mainEP8_IO_FILES4_RNS_12CommunicatorE+0x2b2a)[0x7f563e357f8a]
[fv-az1020-199:05914] [20] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10CLToolMain3runEiPPcP8_IO_FILES4_RNS_12CommunicatorE+0x7d2)[0x7f563e627162]
[fv-az1020-199:05914] [21] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10CLToolMain3cmdESt17basic_string_viewIcSt11char_traitsIcEERKNS_11TypesafePtrE+0x53e)[0x7f563e629bce]
[fv-az1020-199:05914] [22] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain3cmdESt17basic_string_viewIcSt11char_traitsIcEERKNS_11TypesafePtrE+0x12d4)[0x7f563e673964]
[fv-az1020-199:05914] [23] /home/runner/opt/lib/libplumed_masterKernel.so(+0x87d041)[0x7f563e67d041]
[fv-az1020-199:05914] [24] plumed_master(+0x1e1e7)[0x55891eef91e7]
[fv-az1020-199:05914] [25] plumed_master(+0x14d41)[0x55891eeefd41]
[fv-az1020-199:05914] [26] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f563d629d90]
[fv-az1020-199:05914] [27] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f563d629e40]
[fv-az1020-199:05914] [28] plumed_master(+0x14eb5)[0x55891eeefeb5]
[fv-az1020-199:05914] *** End of error message ***
</pre>
{% endraw %}
