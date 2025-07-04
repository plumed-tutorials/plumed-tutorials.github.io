Stderr for source:  RMSD.md_working_7.dat   
Download: [zipped raw stdout](RMSD.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PDB2CONSTANT LABEL=rmsd_ref REFERENCE=reference.pdb
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:37416] *** Process received signal ***
[pkrvmbietmlfzoi:37416] Signal: Aborted (6)
[pkrvmbietmlfzoi:37416] Signal code:  (-6)
[pkrvmbietmlfzoi:37416] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6db7245330]
[pkrvmbietmlfzoi:37416] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6db729eb2c]
[pkrvmbietmlfzoi:37416] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6db724527e]
[pkrvmbietmlfzoi:37416] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6db72288ff]
[pkrvmbietmlfzoi:37416] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6db76a5ff5]
[pkrvmbietmlfzoi:37416] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6db76bb0da]
[pkrvmbietmlfzoi:37416] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6db76a5a55]
[pkrvmbietmlfzoi:37416] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6db76a5a6f]
[pkrvmbietmlfzoi:37416] [ 8] plumed(+0x13209)[0x5604793c9209]
[pkrvmbietmlfzoi:37416] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6db722a1ca]
[pkrvmbietmlfzoi:37416] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6db722a28b]
[pkrvmbietmlfzoi:37416] [11] plumed(+0x134a5)[0x5604793c94a5]
[pkrvmbietmlfzoi:37416] *** End of error message ***
</pre>
{% endraw %}
