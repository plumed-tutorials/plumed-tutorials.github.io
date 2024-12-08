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
[fv-az1778-96:05665] *** Process received signal ***
[fv-az1778-96:05665] Signal: Aborted (6)
[fv-az1778-96:05665] Signal code:  (-6)
[fv-az1778-96:05665] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4546442520]
[fv-az1778-96:05665] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f45464969fc]
[fv-az1778-96:05665] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4546442476]
[fv-az1778-96:05665] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f45464287f3]
[fv-az1778-96:05665] [ 4] /lib/x86_64-linux-gnu/libfabric.so.1(+0x76b4e)[0x7f452b126b4e]
[fv-az1778-96:05665] [ 5] /lib/x86_64-linux-gnu/libc.so.6(+0xeaf48)[0x7f45464eaf48]
[fv-az1778-96:05665] [ 6] /lib/x86_64-linux-gnu/libc.so.6(__libc_fork+0x71)[0x7f45464ea711]
[fv-az1778-96:05665] [ 7] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10SubprocessC2ERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xbc)[0x7f45477a4f2c]
[fv-az1778-96:05665] [ 8] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14GenericMolInfo15interpretSymbolERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt6vectorINS_10AtomNumberESaISA_EE+0x163c)[0x7f454729d6ec]
[fv-az1778-96:05665] [ 9] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic17interpretAtomListERSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EERS1_INS_10AtomNumberESaISB_EE+0x547)[0x7f454725ad87]
[fv-az1778-96:05665] [10] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD15ActionAtomistic13parseAtomListERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEiRSt6vectorINS_10AtomNumberESaISA_EE+0xf1)[0x7f454725b531]
[fv-az1778-96:05665] [11] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD6colvar8GyrationC1ERKNS_13ActionOptionsE+0xf1)[0x7f45472238d1]
[fv-az1778-96:05665] [12] /home/runner/opt/lib/libplumedKernel.so(+0x623fd7)[0x7f4547223fd7]
[fv-az1778-96:05665] [13] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD14ActionRegister6createERKNS_13ActionOptionsE+0x5fc)[0x7f4547260f3c]
[fv-az1778-96:05665] [14] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain14readInputWordsERKSt6vectorINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEESaIS7_EE+0x288)[0x7f45472b6068]
[fv-az1778-96:05665] [15] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERNS_5IFileE+0x54)[0x7f45472b6504]
[fv-az1778-96:05665] [16] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain13readInputFileERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE+0xa6)[0x7f45472b8cd6]
[fv-az1778-96:05665] [17] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain4initEv+0x13ba)[0x7f45472ba26a]
[fv-az1778-96:05665] [18] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x2566)[0x7f45472bcd76]
[fv-az1778-96:05665] [19] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD7cltools6DriverIdE4mainEP8_IO_FILES4_RNS_12CommunicatorE+0x314e)[0x7f4547045fbe]
[fv-az1778-96:05665] [20] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3runEiPPcP8_IO_FILES4_RNS_12CommunicatorE+0x7d3)[0x7f454727b873]
[fv-az1778-96:05665] [21] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10CLToolMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x67e)[0x7f454727e4ae]
[fv-az1778-96:05665] [22] /home/runner/opt/lib/libplumedKernel.so(_ZN4PLMD10PlumedMain3cmdERKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERKNS_11TypesafePtrE+0x208d)[0x7f45472bc89d]
[fv-az1778-96:05665] [23] /home/runner/opt/lib/libplumedKernel.so(+0x6c2dd5)[0x7f45472c2dd5]
[fv-az1778-96:05665] [24] plumed(+0x1a6f0)[0x564dc61cd6f0]
[fv-az1778-96:05665] [25] plumed(+0x1364e)[0x564dc61c664e]
[fv-az1778-96:05665] [26] plumed(+0x1311c)[0x564dc61c611c]
[fv-az1778-96:05665] [27] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4546429d90]
[fv-az1778-96:05665] [28] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4546429e40]
[fv-az1778-96:05665] [29] plumed(+0x131e5)[0x564dc61c61e5]
[fv-az1778-96:05665] *** End of error message ***
</pre>
{% endraw %}
