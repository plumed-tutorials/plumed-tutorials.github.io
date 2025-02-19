Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DUMPPDB ATOMS=cc_data ATOM_INDICES=@nonhydrogens FILE=traj.pdb
Maybe a missing space or a typo?
[fv-az1690-151:06506] *** Process received signal ***
[fv-az1690-151:06506] Signal: Aborted (6)
[fv-az1690-151:06506] Signal code:  (-6)
[fv-az1690-151:06506] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4a33645330]
[fv-az1690-151:06506] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4a3369eb2c]
[fv-az1690-151:06506] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4a3364527e]
[fv-az1690-151:06506] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4a336288ff]
[fv-az1690-151:06506] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4a33aa5ff5]
[fv-az1690-151:06506] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4a33abb0da]
[fv-az1690-151:06506] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4a33aa5a55]
[fv-az1690-151:06506] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4a33aa5a6f]
[fv-az1690-151:06506] [ 8] plumed(+0x13209)[0x55e67b7ea209]
[fv-az1690-151:06506] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4a3362a1ca]
[fv-az1690-151:06506] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4a3362a28b]
[fv-az1690-151:06506] [11] plumed(+0x134a5)[0x55e67b7ea4a5]
[fv-az1690-151:06506] *** End of error message ***
</pre>
{% endraw %}
