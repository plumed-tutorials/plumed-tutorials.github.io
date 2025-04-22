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
[fv-az2211-783:07271] *** Process received signal ***
[fv-az2211-783:07271] Signal: Aborted (6)
[fv-az2211-783:07271] Signal code:  (-6)
[fv-az2211-783:07271] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2b0ca45330]
[fv-az2211-783:07271] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2b0ca9eb2c]
[fv-az2211-783:07271] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2b0ca4527e]
[fv-az2211-783:07271] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2b0ca288ff]
[fv-az2211-783:07271] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2b0cea5ff5]
[fv-az2211-783:07271] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2b0cebb0da]
[fv-az2211-783:07271] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2b0cea5a55]
[fv-az2211-783:07271] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2b0cea5a6f]
[fv-az2211-783:07271] [ 8] plumed(+0x13209)[0x55f0948a5209]
[fv-az2211-783:07271] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2b0ca2a1ca]
[fv-az2211-783:07271] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2b0ca2a28b]
[fv-az2211-783:07271] [11] plumed(+0x134a5)[0x55f0948a54a5]
[fv-az2211-783:07271] *** End of error message ***
</pre>
{% endraw %}
