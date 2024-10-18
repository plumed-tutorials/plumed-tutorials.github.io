Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed_master.stderr.txt.zip) 
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
[fv-az665-16:70611] *** Process received signal ***
[fv-az665-16:70611] Signal: Aborted (6)
[fv-az665-16:70611] Signal code:  (-6)
[fv-az665-16:70611] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f478d642520]
[fv-az665-16:70611] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f478d6969fc]
[fv-az665-16:70611] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f478d642476]
[fv-az665-16:70611] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f478d6287f3]
[fv-az665-16:70611] [ 4] /lib/x86_64-linux-gnu/libfabric.so.1(+0x76b4e)[0x7f4772321b4e]
[fv-az665-16:70611] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0xeaf48)[0x7f478d6eaf48]
[fv-az665-16:70611] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_fork+0x71)[0x7f478d6ea711]
[fv-az665-16:70611] [ 7] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10SubprocessC2ERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xc1)[0x7f478ed88321]
[fv-az665-16:70611] [ 8] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD14GenericMolInfo15interpretSymbolERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt6vectorINS_10AtomNumberESaISA_EE+0x162b)[0x7f478e65808b]
[fv-az665-16:70611] [ 9] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD15ActionAtomistic17interpretAtomListERSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERKS1_IPNS_5ValueESaISC_EEPNS_6ActionERS1_INS_10AtomNumberESaISJ_EE+0x6c1)[0x7f478e5dea51]
[fv-az665-16:70611] [10] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD15ActionAtomistic13parseAtomListERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEiRSt6vectorINS_10AtomNumberESaISA_EE+0x10d)[0x7f478e5dffcd]
[fv-az665-16:70611] [11] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD6colvar8GyrationC1ERKNS_13ActionOptionsE+0x103)[0x7f478e547023]
[fv-az665-16:70611] [12] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD18ActionRegistrationINS_6colvar8GyrationEE6createERKNS_13ActionOptionsE+0x27)[0x7f478e54a167]
[fv-az665-16:70611] [13] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD14ActionRegister6createERKSt6vectorIPvSaIS2_EERKNS_13ActionOptionsE+0x3f9)[0x7f478e5e33f9]
[fv-az665-16:70611] [14] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain14readInputWordsERKSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERKb+0x2da)[0x7f478e66b67a]
[fv-az665-16:70611] [15] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain13readInputLineERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKb+0xba)[0x7f478e66ba3a]
[fv-az665-16:70611] [16] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD14ActionShortcut13readInputLineERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEb+0x2d3)[0x7f478e5ef8f3]
[fv-az665-16:70611] [17] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD6colvar16GyrationShortcutC1ERKNS_13ActionOptionsE+0x538)[0x7f478e550358]
[fv-az665-16:70611] [18] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD18ActionRegistrationINS_6colvar16GyrationShortcutEE6createERKNS_13ActionOptionsE+0x27)[0x7f478e554b27]
[fv-az665-16:70611] [19] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD14ActionRegister6createERKSt6vectorIPvSaIS2_EERKNS_13ActionOptionsE+0x3f9)[0x7f478e5e33f9]
[fv-az665-16:70611] [20] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain14readInputWordsERKSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERKb+0x2da)[0x7f478e66b67a]
[fv-az665-16:70611] [21] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain13readInputFileERNS_5IFileE+0x5c)[0x7f478e66be2c]
[fv-az665-16:70611] [22] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain13readInputFileERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0x9f)[0x7f478e67153f]
[fv-az665-16:70611] [23] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain4initEv+0xb6a)[0x7f478e67211a]
[fv-az665-16:70611] [24] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain3cmdESt17basic_string_viewIcSt11char_traitsIcEERKNS_11TypesafePtrE+0x29bf)[0x7f478e6750bf]
[fv-az665-16:70611] [25] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD7cltools6DriverIdE4mainEP8_IO_FILES4_RNS_12CommunicatorE+0x2b2a)[0x7f478e357f7a]
[fv-az665-16:70611] [26] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10CLToolMain3runEiPPcP8_IO_FILES4_RNS_12CommunicatorE+0x7d2)[0x7f478e6271d2]
[fv-az665-16:70611] [27] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10CLToolMain3cmdESt17basic_string_viewIcSt11char_traitsIcEERKNS_11TypesafePtrE+0x53e)[0x7f478e629c3e]
[fv-az665-16:70611] [28] /home/runner/opt/lib/libplumed_masterKernel.so(_ZN4PLMD10PlumedMain3cmdESt17basic_string_viewIcSt11char_traitsIcEERKNS_11TypesafePtrE+0x12d4)[0x7f478e6739d4]
[fv-az665-16:70611] [29] /home/runner/opt/lib/libplumed_masterKernel.so(+0x87d0b1)[0x7f478e67d0b1]
[fv-az665-16:70611] *** End of error message ***
</pre>
{% endraw %}
