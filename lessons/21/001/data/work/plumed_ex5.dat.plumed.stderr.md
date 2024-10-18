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
[fv-az665-16:70648] *** Process received signal ***
[fv-az665-16:70648] Signal: Aborted (6)
[fv-az665-16:70648] Signal code:  (-6)
[fv-az665-16:70648] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4636642520]
[fv-az665-16:70648] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f46366969fc]
[fv-az665-16:70648] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4636642476]
[fv-az665-16:70648] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f46366287f3]
[fv-az665-16:70648] [ 4] /lib/x86_64-linux-gnu/libfabric.so.1(+0x76b4e)[0x7f461b298b4e]
[fv-az665-16:70648] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0xeaf48)[0x7f46366eaf48]
[fv-az665-16:70648] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_fork+0x71)[0x7f46366ea711]
[fv-az665-16:70648] [ 7] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10SubprocessC2ERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xbc)[0x7f46379a4f2c]
[fv-az665-16:70648] [ 8] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14GenericMolInfo15interpretSymbolERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt6vectorINS_10AtomNumberESaISA_EE+0x163c)[0x7f463749d6ec]
[fv-az665-16:70648] [ 9] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic17interpretAtomListERSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERS1_INS_10AtomNumberESaISB_EE+0x547)[0x7f463745ad87]
[fv-az665-16:70648] [10] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic13parseAtomListERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEiRSt6vectorINS_10AtomNumberESaISA_EE+0xf1)[0x7f463745b531]
[fv-az665-16:70648] [11] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD7generic14WholeMoleculesC1ERKNS_13ActionOptionsE+0x23e)[0x7f46376015de]
[fv-az665-16:70648] [12] /home/runner/opt/lib/libplumedKernel.so(+0x802617)[0x7f4637602617]
[fv-az665-16:70648] [13] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14ActionRegister6createERKNS_13ActionOptionsE+0x5fc)[0x7f4637460f3c]
[fv-az665-16:70648] [14] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain14readInputWordsERKSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EE+0x288)[0x7f46374b6068]
[fv-az665-16:70648] [15] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERNS_5IFileE+0x54)[0x7f46374b6504]
[fv-az665-16:70648] [16] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xa6)[0x7f46374b8cd6]
[fv-az665-16:70648] [17] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain4initEv+0x13ba)[0x7f46374ba26a]
[fv-az665-16:70648] [18] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x2566)[0x7f46374bcd76]
[fv-az665-16:70648] [19] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD7cltools6DriverIdE4mainEP8_IO_FILES4_RNS_12CommunicatorE+0x314e)[0x7f4637245fbe]
[fv-az665-16:70648] [20] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3runEiPPcP8_IO_FILES4_RNS_12CommunicatorE+0x7d3)[0x7f463747b873]
[fv-az665-16:70648] [21] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x67e)[0x7f463747e4ae]
[fv-az665-16:70648] [22] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x208d)[0x7f46374bc89d]
[fv-az665-16:70648] [23] /home/runner/opt/lib/libplumedKernel.so(+0x6c2dd5)[0x7f46374c2dd5]
[fv-az665-16:70648] [24] plumed(+0x1a6f0)[0x5653c7d6b6f0]
[fv-az665-16:70648] [25] plumed(+0x1364e)[0x5653c7d6464e]
[fv-az665-16:70648] [26] plumed(+0x1311c)[0x5653c7d6411c]
[fv-az665-16:70648] [27] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4636629d90]
[fv-az665-16:70648] [28] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4636629e40]
[fv-az665-16:70648] [29] plumed(+0x131e5)[0x5653c7d641e5]
[fv-az665-16:70648] *** End of error message ***
</pre>
{% endraw %}
