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
[fv-az1020-199:05906] *** Process received signal ***
[fv-az1020-199:05906] Signal: Aborted (6)
[fv-az1020-199:05906] Signal code:  (-6)
[fv-az1020-199:05906] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4b66642520]
[fv-az1020-199:05906] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f4b666969fc]
[fv-az1020-199:05906] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4b66642476]
[fv-az1020-199:05906] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f4b666287f3]
[fv-az1020-199:05906] [ 4] /lib/x86_64-linux-gnu/libfabric.so.1(+0x76b4e)[0x7f4b4b321b4e]
[fv-az1020-199:05906] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0xeaf48)[0x7f4b666eaf48]
[fv-az1020-199:05906] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_fork+0x71)[0x7f4b666ea711]
[fv-az1020-199:05906] [ 7] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10SubprocessC2ERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xbc)[0x7f4b679a4f5c]
[fv-az1020-199:05906] [ 8] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14GenericMolInfo15interpretSymbolERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt6vectorINS_10AtomNumberESaISA_EE+0x163c)[0x7f4b6749d71c]
[fv-az1020-199:05906] [ 9] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic17interpretAtomListERSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERS1_INS_10AtomNumberESaISB_EE+0x547)[0x7f4b6745adb7]
[fv-az1020-199:05906] [10] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic13parseAtomListERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEiRSt6vectorINS_10AtomNumberESaISA_EE+0xf1)[0x7f4b6745b561]
[fv-az1020-199:05906] [11] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD7generic14WholeMoleculesC1ERKNS_13ActionOptionsE+0x23e)[0x7f4b6760160e]
[fv-az1020-199:05906] [12] /home/runner/opt/lib/libplumedKernel.so(+0x802647)[0x7f4b67602647]
[fv-az1020-199:05906] [13] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14ActionRegister6createERKNS_13ActionOptionsE+0x5fc)[0x7f4b67460f6c]
[fv-az1020-199:05906] [14] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain14readInputWordsERKSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EE+0x288)[0x7f4b674b6098]
[fv-az1020-199:05906] [15] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERNS_5IFileE+0x54)[0x7f4b674b6534]
[fv-az1020-199:05906] [16] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xa6)[0x7f4b674b8d06]
[fv-az1020-199:05906] [17] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain4initEv+0x13ba)[0x7f4b674ba29a]
[fv-az1020-199:05906] [18] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x2566)[0x7f4b674bcda6]
[fv-az1020-199:05906] [19] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD7cltools6DriverIdE4mainEP8_IO_FILES4_RNS_12CommunicatorE+0x314e)[0x7f4b67245fae]
[fv-az1020-199:05906] [20] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3runEiPPcP8_IO_FILES4_RNS_12CommunicatorE+0x7d3)[0x7f4b6747b8a3]
[fv-az1020-199:05906] [21] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x67e)[0x7f4b6747e4de]
[fv-az1020-199:05906] [22] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x208d)[0x7f4b674bc8cd]
[fv-az1020-199:05906] [23] /home/runner/opt/lib/libplumedKernel.so(+0x6c2e05)[0x7f4b674c2e05]
[fv-az1020-199:05906] [24] plumed(+0x1a6f0)[0x5610f59266f0]
[fv-az1020-199:05906] [25] plumed(+0x1364e)[0x5610f591f64e]
[fv-az1020-199:05906] [26] plumed(+0x1311c)[0x5610f591f11c]
[fv-az1020-199:05906] [27] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4b66629d90]
[fv-az1020-199:05906] [28] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4b66629e40]
[fv-az1020-199:05906] [29] plumed(+0x131e5)[0x5610f591f1e5]
[fv-az1020-199:05906] *** End of error message ***
</pre>
{% endraw %}
