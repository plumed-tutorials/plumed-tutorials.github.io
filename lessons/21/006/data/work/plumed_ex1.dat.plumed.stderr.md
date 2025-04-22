Stderr for source:  work/plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed.stderr.txt.zip) 
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
[fv-az2211-783:07175] *** Process received signal ***
[fv-az2211-783:07175] Signal: Aborted (6)
[fv-az2211-783:07175] Signal code:  (-6)
[fv-az2211-783:07175] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f95a9445330]
[fv-az2211-783:07175] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f95a949eb2c]
[fv-az2211-783:07175] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f95a944527e]
[fv-az2211-783:07175] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f95a94288ff]
[fv-az2211-783:07175] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f95a98a5ff5]
[fv-az2211-783:07175] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f95a98bb0da]
[fv-az2211-783:07175] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f95a98a5a55]
[fv-az2211-783:07175] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f95a98a5a6f]
[fv-az2211-783:07175] [ 8] plumed(+0x13209)[0x55f3c2a09209]
[fv-az2211-783:07175] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f95a942a1ca]
[fv-az2211-783:07175] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f95a942a28b]
[fv-az2211-783:07175] [11] plumed(+0x134a5)[0x55f3c2a094a5]
[fv-az2211-783:07175] *** End of error message ***
</pre>
{% endraw %}
