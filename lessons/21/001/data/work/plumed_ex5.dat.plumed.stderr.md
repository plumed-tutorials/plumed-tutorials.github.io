Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed.stderr.txt.zip) 
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
[fv-az1778-96:05710] *** Process received signal ***
[fv-az1778-96:05710] Signal: Aborted (6)
[fv-az1778-96:05710] Signal code:  (-6)
[fv-az1778-96:05710] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fcca5842520]
[fv-az1778-96:05710] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fcca58969fc]
[fv-az1778-96:05710] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fcca5842476]
[fv-az1778-96:05710] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fcca58287f3]
[fv-az1778-96:05710] [ 4] /lib/x86_64-linux-gnu/libfabric.so.1(+0x76b4e)[0x7fcc8a921b4e]
[fv-az1778-96:05710] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0xeaf48)[0x7fcca58eaf48]
[fv-az1778-96:05710] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_fork+0x71)[0x7fcca58ea711]
[fv-az1778-96:05710] [ 7] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10SubprocessC2ERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xbc)[0x7fcca6ba4f2c]
[fv-az1778-96:05710] [ 8] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14GenericMolInfo15interpretSymbolERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt6vectorINS_10AtomNumberESaISA_EE+0x163c)[0x7fcca669d6ec]
[fv-az1778-96:05710] [ 9] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic17interpretAtomListERSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERS1_INS_10AtomNumberESaISB_EE+0x547)[0x7fcca665ad87]
[fv-az1778-96:05710] [10] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic13parseAtomListERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEiRSt6vectorINS_10AtomNumberESaISA_EE+0xf1)[0x7fcca665b531]
[fv-az1778-96:05710] [11] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD7generic14WholeMoleculesC1ERKNS_13ActionOptionsE+0x23e)[0x7fcca68015de]
[fv-az1778-96:05710] [12] /home/runner/opt/lib/libplumedKernel.so(+0x802617)[0x7fcca6802617]
[fv-az1778-96:05710] [13] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14ActionRegister6createERKNS_13ActionOptionsE+0x5fc)[0x7fcca6660f3c]
[fv-az1778-96:05710] [14] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain14readInputWordsERKSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EE+0x288)[0x7fcca66b6068]
[fv-az1778-96:05710] [15] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERNS_5IFileE+0x54)[0x7fcca66b6504]
[fv-az1778-96:05710] [16] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xa6)[0x7fcca66b8cd6]
[fv-az1778-96:05710] [17] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain4initEv+0x13ba)[0x7fcca66ba26a]
[fv-az1778-96:05710] [18] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x2566)[0x7fcca66bcd76]
[fv-az1778-96:05710] [19] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD7cltools6DriverIdE4mainEP8_IO_FILES4_RNS_12CommunicatorE+0x314e)[0x7fcca6445fbe]
[fv-az1778-96:05710] [20] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3runEiPPcP8_IO_FILES4_RNS_12CommunicatorE+0x7d3)[0x7fcca667b873]
[fv-az1778-96:05710] [21] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x67e)[0x7fcca667e4ae]
[fv-az1778-96:05710] [22] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x208d)[0x7fcca66bc89d]
[fv-az1778-96:05710] [23] /home/runner/opt/lib/libplumedKernel.so(+0x6c2dd5)[0x7fcca66c2dd5]
[fv-az1778-96:05710] [24] plumed(+0x1a6f0)[0x5576aea976f0]
[fv-az1778-96:05710] [25] plumed(+0x1364e)[0x5576aea9064e]
[fv-az1778-96:05710] [26] plumed(+0x1311c)[0x5576aea9011c]
[fv-az1778-96:05710] [27] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fcca5829d90]
[fv-az1778-96:05710] [28] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fcca5829e40]
[fv-az1778-96:05710] [29] plumed(+0x131e5)[0x5576aea901e5]
[fv-az1778-96:05710] *** End of error message ***
</pre>
{% endraw %}
