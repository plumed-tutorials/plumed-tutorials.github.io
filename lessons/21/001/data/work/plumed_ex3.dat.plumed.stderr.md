Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
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
[fv-az665-16:70603] *** Process received signal ***
[fv-az665-16:70603] Signal: Aborted (6)
[fv-az665-16:70603] Signal code:  (-6)
[fv-az665-16:70603] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fb4f7242520]
[fv-az665-16:70603] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fb4f72969fc]
[fv-az665-16:70603] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fb4f7242476]
[fv-az665-16:70603] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fb4f72287f3]
[fv-az665-16:70603] [ 4] /lib/x86_64-linux-gnu/libfabric.so.1(+0x76b4e)[0x7fb4dbd26b4e]
[fv-az665-16:70603] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0xeaf48)[0x7fb4f72eaf48]
[fv-az665-16:70603] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_fork+0x71)[0x7fb4f72ea711]
[fv-az665-16:70603] [ 7] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10SubprocessC2ERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xbc)[0x7fb4f85a4f2c]
[fv-az665-16:70603] [ 8] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14GenericMolInfo15interpretSymbolERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt6vectorINS_10AtomNumberESaISA_EE+0x163c)[0x7fb4f809d6ec]
[fv-az665-16:70603] [ 9] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic17interpretAtomListERSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERS1_INS_10AtomNumberESaISB_EE+0x547)[0x7fb4f805ad87]
[fv-az665-16:70603] [10] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic13parseAtomListERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEiRSt6vectorINS_10AtomNumberESaISA_EE+0xf1)[0x7fb4f805b531]
[fv-az665-16:70603] [11] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD6colvar8GyrationC1ERKNS_13ActionOptionsE+0xf1)[0x7fb4f80238d1]
[fv-az665-16:70603] [12] /home/runner/opt/lib/libplumedKernel.so(+0x623fd7)[0x7fb4f8023fd7]
[fv-az665-16:70603] [13] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14ActionRegister6createERKNS_13ActionOptionsE+0x5fc)[0x7fb4f8060f3c]
[fv-az665-16:70603] [14] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain14readInputWordsERKSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EE+0x288)[0x7fb4f80b6068]
[fv-az665-16:70603] [15] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERNS_5IFileE+0x54)[0x7fb4f80b6504]
[fv-az665-16:70603] [16] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xa6)[0x7fb4f80b8cd6]
[fv-az665-16:70603] [17] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain4initEv+0x13ba)[0x7fb4f80ba26a]
[fv-az665-16:70603] [18] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x2566)[0x7fb4f80bcd76]
[fv-az665-16:70603] [19] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD7cltools6DriverIdE4mainEP8_IO_FILES4_RNS_12CommunicatorE+0x314e)[0x7fb4f7e45fbe]
[fv-az665-16:70603] [20] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3runEiPPcP8_IO_FILES4_RNS_12CommunicatorE+0x7d3)[0x7fb4f807b873]
[fv-az665-16:70603] [21] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x67e)[0x7fb4f807e4ae]
[fv-az665-16:70603] [22] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x208d)[0x7fb4f80bc89d]
[fv-az665-16:70603] [23] /home/runner/opt/lib/libplumedKernel.so(+0x6c2dd5)[0x7fb4f80c2dd5]
[fv-az665-16:70603] [24] plumed(+0x1a6f0)[0x557512c1c6f0]
[fv-az665-16:70603] [25] plumed(+0x1364e)[0x557512c1564e]
[fv-az665-16:70603] [26] plumed(+0x1311c)[0x557512c1511c]
[fv-az665-16:70603] [27] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fb4f7229d90]
[fv-az665-16:70603] [28] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fb4f7229e40]
[fv-az665-16:70603] [29] plumed(+0x131e5)[0x557512c151e5]
[fv-az665-16:70603] *** End of error message ***
</pre>
{% endraw %}
